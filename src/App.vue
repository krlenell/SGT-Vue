<template>
  <div id="app">
    <Header></Header>
    <!--<HelloWorld
    msg="So this is how props work eh?"
    />-->
    <TodoTable></TodoTable>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import TodoTable from './components/TodoTable.vue'
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    Header,
    TodoTable
    // HelloWorld
  }
}
</script>
