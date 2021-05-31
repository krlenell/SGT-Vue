<template>
  <form @submit.prevent="onSubmit" class="box">
    <b-field label="Student">
      <b-input v-model="student"/>
    </b-field>
    <b-field label="Course">
      <b-input v-model="course"/>
    </b-field>
    <b-field label="Grade">
      <b-input v-model.number="grade"/>
    </b-field>
    <button class="button is-primary" type="submit">Add Student</button>
  </form>
</template>

<script>
export default {
  name: 'GradeInputForm',
  data () {
    return {
      student: '',
      course: '',
      grade: null
    }
  },
  methods: {
    onSubmit () {
      const grade = {
        student: this.student,
        course: this.course,
        grade: this.grade
      }
      for (const key in grade) {
        if (grade[key] === '' || grade[key] === null) {
          alert(key + ' field is empty. Please fill it in.')
          return
        }
      }
      if (typeof grade.grade !== 'number') {
        alert('Please enter a valid number for grade')
        return
      }
      this.$emit('grade-submitted', grade)

      this.student = ''
      this.course = ''
      this.grade = null
    }
  }
}
</script>
