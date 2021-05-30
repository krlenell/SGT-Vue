<template>
  <div id="app">
    <Header></Header>
    <TodoTable :todos="todos"></TodoTable>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import TodoTable from './components/TodoTable.vue'

export default {
  name: 'App',
  components: {
    Header,
    TodoTable
  },
  data () {
    return {
      todos: [
        { id: 1, task: 'Get Groceries' }
      ]
    }
  }
}
</script>
