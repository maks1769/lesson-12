<template>
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <div class="d-flex flex-column flex-md-row align-items-center p-3 px-md-4 mb-3 bg-white border-bottom box-shadow">
          <h5 class="my-0 mr-md-auto font-weight-normal">Nuxt project</h5>
          <nav class="my-2 my-md-0 mr-md-3">
            <nuxt-link class="p-2 text-dark" no-prefetch to="/">Home</nuxt-link>
            <nuxt-link class="p-2 text-dark" to="/about">About</nuxt-link>
            <nuxt-link class="p-2 text-dark" no-prefetch to="/posts">Posts</nuxt-link>
          </nav>
          <a class="btn btn-outline-primary" href="#">Sign up</a>
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-md-12">
        <nuxt/>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "bootstrap"
}
</script>

<style scoped>

</style>
