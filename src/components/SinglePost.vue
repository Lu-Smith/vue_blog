<template>
    <div class="post">
        <h2>{{ post.title }}</h2>
        <p>{{ post.body }}</p>
    </div>
</template>

<script>
export default {
props: ['post']
}
</script>

<style>

</style>