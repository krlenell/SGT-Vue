<template>
  <div id="app">
    <Header></Header>
    <HelloWorld
    msg="So this is how props work eh?"
    class="column is-three-fifths is-offset-one-fifth"
    />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    Header,
    HelloWorld
  }
}
</script>
