<template>
  <div class="home">
    <h1>Hello World</h1>
    <p>My name is {{ name }} and my age is {{ age }}</p>
    <button @click ="handleClick">click me</button>
    <input type="text" v-model="name">
  </div>
</template>

<script>
// @ is an alias to /src
import { ref } from 'vue'

export default {
  name: 'HomeView',
  setup() {

    let name = ref('lucy')
    let age = ref(30)

    const handleClick = () => {
      name.value = 'luigi'
      age.value = '23'
    }

    return {name, age, handleClick }
  }
}
</script>
