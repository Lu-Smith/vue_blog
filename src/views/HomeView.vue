<template>
  <div class="home">
    <h1>Hello World</h1>
    <p ref="p">My name is {{ name }} and my age is {{ age }}</p>
    <button @click ="handleClick">click me</button>
  </div>
</template>

<script>
// @ is an alias to /src
import { ref } from 'vue'

export default {
  name: 'HomeView',
  setup() {
    console.log(this)

    const p = ref(null)
    let name = 'lucy'
    let age = 30

    const handleClick = () => {
      console.log(p,p.value)
      p.value.classList.add('test')
      p.value.textContent = 'hello'
    }

    return {name, age, handleClick, p}
  }
}
</script>
