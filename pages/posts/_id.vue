<template>
  <div>
    <h3>Post #{{ posts.id }}</h3>
    <p>{{ posts.body }}</p>
  </div>
</template>

<script>
import axios from "axios";

export default {
  layout: 'bootstrap',

  async asyncData({params}) {
    return await axios.get(`https://jsonplaceholder.typicode.com/posts/${params.id}`)
      .then(result => {
        return {posts: result.data}
      })
  },
}
</script>

<style scoped>

</style>
