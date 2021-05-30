<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <section>
      <b-button
      @click="clickMe"
      >Click Me!</b-button>
    </section>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    clickMe () {
      this.$buefy.notification.open('I was clicked')
    }
  }
}
</script>
