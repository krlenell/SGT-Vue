<template>
  <b-table :data="data" :columns="columns"></b-table>
</template>

<script>
export default {
  name: 'TodoTable',
  data () {
    return {
      data: [
        { id: 1, task: 'Get Groceries' }
      ],
      columns: [
        {
          field: 'id',
          label: 'Number',
          width: '40',
          numeric: true
        },
        {
          field: 'task',
          label: 'Task'
        }
      ]
    }
  }
}

</script>
