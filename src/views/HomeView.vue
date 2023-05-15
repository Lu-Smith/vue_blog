<template>
  <div class="home">
    <h1>Hello World</h1>
    <p>My name is {{ name }} and my age is {{ age }}</p>
    <button @click ="handleClick">click me</button>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'HomeView',
  setup() {
    let name = 'lucy'
    let age = 30

    const handleClick = () => {
      console.log('you clicked me')
    }

    return {name, age, handleClick}
  }
}
</script>
