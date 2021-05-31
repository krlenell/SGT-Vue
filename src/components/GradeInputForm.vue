<template>
  <form @submit.prevent="onSubmit" class="box">
    <b-field label="Student">
      <b-input v-model="student"></b-input>
    </b-field>
    <b-field label="Course">
      <b-input v-model="course"></b-input>
    </b-field>
    <b-field label="Grade">
      <b-input v-model="grade"></b-input>
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
      grade: ''
    }
  },
  methods: {
    onSubmit () {
      alert('submitted')
      console.log('student', this.student)
      // if not filled out properly, send an alert
    }
  }
}
</script>
