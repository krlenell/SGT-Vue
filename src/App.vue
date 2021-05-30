<template>
  <div id="app">
    <Header></Header>
    <div class="columns">
      <GradeTable :grades="grades" class="column is-three-fifths"></GradeTable>
      <GradeInputForm class="column"></GradeInputForm>
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
      grades: [
        { id: 1, student: 'Ted Theodore Logan', course: 'History', grade: 100 },
        { id: 2, student: 'Tommy Bahama', course: 'Alphabet', grade: 20 }
      ]
    }
  }
}
</script>
