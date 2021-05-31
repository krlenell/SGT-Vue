<template>
  <div id="app">
    <Header></Header>
    <div class="columns">
      <GradeTable :grades="grades" class="column box is-three-fifths"></GradeTable>
      <GradeInputForm
        class="column"
        @grade-submitted="addGrade"
      ></GradeInputForm>
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import GradeTable from './components/GradeTable.vue'
import GradeInputForm from './components/GradeInputForm.vue'

export default {
  name: 'App',
  components: {
    Header,
    GradeTable,
    GradeInputForm
  },
  data () {
    return {
      nextId: 3,
      grades: [
        { id: 1, student: 'Ted Theodore Logan', course: 'History', grade: 100 },
        { id: 2, student: 'Tommy Bahama', course: 'Alphabet', grade: 20 }
      ]
    }
  },
  methods: {
    addGrade (grade) {
      console.log('added grade', grade)
      grade.id = this.nextId
      this.grades.push(grade)
      console.log('pushed grade', this.grades)
      this.nextId++
    }
  }
}
</script>
