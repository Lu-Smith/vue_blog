<template>
  <div class="home">
    <h1>Home</h1>
    <input type="text" v-model="search">
    <div v-for="name in names" :key="name">{{ name }}</div>
  </div>
</template>

<script>
// @ is an alias to /src
import { computed, ref} from 'vue'

export default {
  name: 'HomeView',
  setup() {
    const search = ref('')
    const names = ref(['mario', 'yoshi', 'luigi', 'toad', 'browser', 'koopa', 'peach'])
    return { names, search }
  }
}
</script>
