<template>
  <div class="home">
    <h1>Home</h1>
  </div>
  <p>{{ name }}</p>
</template>

<script>
// @ is an alias to /src
import { computed, ref} from 'vue'

export default {
  name: 'HomeView',
  setup() {
    const name = computed(() => {
      return 'shaun'
    })
    return { name }
  }
}
</script>
