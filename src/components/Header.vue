<template>
  <header class="navbar is-primary">
    <div class="navbar-brand">
      <font-awesome-icon :icon="list" size="6x" color="teal" class="navbar-item"></font-awesome-icon>
    </div>
  </header>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faClipboardList } from '@fortawesome/free-solid-svg-icons'

export default {
  name: 'Header',
  components: { FontAwesomeIcon },
  data () {
    return {
      list: faClipboardList
    }
  }
}
</script>
