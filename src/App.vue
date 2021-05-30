<template>
  <div id="app">
    <HelloWorld
    msg="So this is how props work eh?"
    class="column is-three-fifths is-offset-one-fifth"
    />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>
