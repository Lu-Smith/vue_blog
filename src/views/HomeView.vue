<template>
  <div class="home">
    <h1>Refs</h1>
    <p>{{ ninjaOne.name }} - {{ ninjaOne.age }}</p>
    <button @click ="updateNinjaOne">Update Ninja one</button>
  </div>
</template>

<script>
// @ is an alias to /src
import { ref } from 'vue'

export default {
  name: 'HomeView',
  setup() {

    const ninjaOne = ref({ name:'mario', age: 30})

    const updateNinjaOne = () => {
      ninjaOne.value.age = 40
    }

    return { ninjaOne, updateNinjaOne }
  }
}
</script>
