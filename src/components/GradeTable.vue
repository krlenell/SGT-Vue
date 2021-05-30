<template>
  <div>
    <b-table :data="grades" :columns="columns"></b-table>
  </div>
</template>

<script>
export default {
  name: 'GradeTable',
  props: {
    grades: Array
  },
  data () {
    return {
      columns: [
        {
          field: 'id',
          label: 'Number',
          width: '40',
          numeric: true
        },
        {
          field: 'student',
          label: 'Student'
        },
        {
          field: 'course',
          label: 'Course'
        },
        {
          field: 'grade',
          label: 'Grade'
        }
      ]
    }
  }
}

</script>
