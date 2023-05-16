<template>
  <div class="home">
    <h1>Refs</h1>
    <p>{{ ninjaOne.name }} - {{ ninjaOne.age }}</p>
    <button @click ="updateNinjaOne">Update Ninja one</button>
    <h1>Rective</h1>
    <p>{{ ninjaTwo.name }} - {{ ninjaTwo.age }}</p>
    <button @click ="updateNinjaTwo">Update Ninja two</button>
  </div>
</template>

<script>
// @ is an alias to /src
import { ref, reactive } from 'vue'

export default {
  name: 'HomeView',
  setup() {

    const ninjaOne = ref({ name:'mario', age: 30})
    const ninjaTwo = reactive({ name:'luna', age: 35})

    const updateNinjaOne = () => {
      ninjaOne.value.age = 40
    }

    const updateNinjaTwo = () => {
      ninjaTwo.age = 40
    }

    return { ninjaOne, ninjaTwo, updateNinjaOne, updateNinjaTwo }
  }
}
</script>
