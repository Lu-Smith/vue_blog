<template>
  <div class="home">
    <h1>Hello World</h1>
    <p>My name is {{ name }} and my age is {{ age }}</p>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'HomeView',
  setup() {
    console.log('setup')
    let name = 'lucy'
    let age = 30

    return {name, age}
  }
}
</script>
