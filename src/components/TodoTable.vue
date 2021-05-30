<template>
  <b-table :data="todos" :columns="columns"></b-table>
</template>

<script>
export default {
  name: 'TodoTable',
  props: {
    todos: Array
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
          field: 'task',
          label: 'Task'
        }
      ]
    }
  }
}

</script>
