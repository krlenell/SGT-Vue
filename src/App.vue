<template>
  <div id="app">
    <Header></Header>
    <GradeTable :grades="grades"></GradeTable>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import GradeTable from './components/GradeTable.vue'

export default {
  name: 'App',
  components: {
    Header,
    GradeTable
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
