<template>
  <div class="home">
    <h1>Home</h1>
    <PostList v-if="showPosts" :posts="posts"/>
    <button @click="showPosts = !showPosts">toggle posts</button>

  </div>
</template>

<script>
import PostList from '../components/PostList.vue'
import {ref} from 'vue'

export default {
  name: 'HomeView',
  components: {
    PostList
  },
  setup() {
    const posts = ref([
      {title: 'welcome to the blog', body: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus alias animi suscipit error numquam ea ratione? Fugit nesciunt voluptatibus iste saepe sunt dolor suscipit doloribus eius molestias debitis, accusantium commodi rem illo dolores velit voluptates corrupti sapiente qui. Dignissimos est et laboriosam quisquam enim expedita obcaecati, ducimus quod, maxime, at minus reiciendis quasi ipsum totam voluptates officia fugiat reprehenderit accusantium sunt? Ducimus voluptate suscipit repellat voluptates reiciendis voluptatibus amet hic labore ratione fugiat reprehenderit quaerat quasi odit tempore inventore consequuntur minus molestias, laborum maxime? Adipisci iure minus soluta vitae aspernatur quod sunt commodi, obcaecati temporibus quis inventore consectetur asperiores corrupti!', id: 1},
      {title: 'top 5 css', body: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus alias animi suscipit error numquam ea ratione? Fugit nesciunt voluptatibus iste saepe sunt dolor suscipit doloribus eius molestias debitis, accusantium commodi rem illo dolores velit voluptates corrupti sapiente qui. Dignissimos est et laboriosam quisquam enim expedita obcaecati, ducimus quod, maxime, at minus reiciendis quasi ipsum totam voluptates officia fugiat reprehenderit accusantium sunt? Ducimus voluptate suscipit repellat voluptates reiciendis voluptatibus amet hic labore ratione fugiat reprehenderit quaerat quasi odit tempore inventore consequuntur minus molestias, laborum maxime? Adipisci iure minus soluta vitae aspernatur quod sunt commodi, obcaecati temporibus quis inventore consectetur asperiores corrupti!', id: 2},
    ])
    const showPosts = ref(true)

    return { posts, showPosts }
  }
}
</script>
