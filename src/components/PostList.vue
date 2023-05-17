<template>
  <div class="post-list">
    <h1>Hello</h1>
    <div v-for="post in posts" :key="post.id" >
        <h3>{{ post.title }}</h3>
    </div>
  </div>
</template>

<script>
export default {
    props: ['posts']
}
</script>

<style>

</style>