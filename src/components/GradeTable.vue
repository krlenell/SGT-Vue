<template>
  <div>
    <b-table
    :data="grades"
    :columns="columns"
    checkable
    checkbox-position="left"
    :checked-rows.sync="checkedRows"
    ></b-table>
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
      checkedRows: [],
      columns: [
        {
          field: 'id',
          label: 'Student ID',
          width: '30',
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
