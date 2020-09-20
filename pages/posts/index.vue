<template>
  <div>
    <h2>Posts list</h2>
    <ul class="list-group list-group-flush text-secondary">
      <li class="list-group-item"
          v-for="item in posts"
          :key="item.id"
      >
        <a href="#" @click.prevent="openPost(item.id)">{{ item.id }} - {{ item.title }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  layout: 'bootstrap',

  async asyncData() {
    return await axios.get('https://jsonplaceholder.typicode.com/posts/')
    .then(result => {
      return {posts: result.data}
    })
  },

  methods: {
    openPost(item) {
      this.$router.push('/posts/' + item)
    }
  }
}
</script>

<style scoped>

</style>
