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
    <b-button type="is-primary" native-type="submit">Add Student</b-button>
    <b-button
      class="delete-button"
      type="is-danger"
    >
      <font-awesome-icon :icon="trash" class="trash-icon"/>Delete
    </b-button>
  </form>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faTrash } from '@fortawesome/free-solid-svg-icons'

export default {
  name: 'GradeInputForm',
  components: { FontAwesomeIcon },
  data () {
    return {
      student: '',
      course: '',
      grade: null,
      trash: faTrash
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

<style scoped>
  .delete-button{
    margin-left: 10px;
  }
  .trash-icon{
    margin-right: 3px;
  }
</style>
