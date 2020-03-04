<template>
  <div class="container">
    <SearchBar />
    <h1 class="title">lets-fight</h1>
    <h2 class="subtitle">My bedazzling Nuxt.js project</h2>
    <div class="links">
      <a href="https://nuxtjs.org/" target="_blank" class="button--green"
        >Documentation</a
      >
      <a
        href="https://github.com/nuxt/nuxt.js"
        target="_blank"
        class="button--grey"
        >GitHub</a
      >
    </div>
  </div>
</template>

<script>
import SearchBar from '~/components/SearchBar'
export default {
  components: {
    SearchBar
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  border: 1px solid rgb(56, 68, 77);
  max-width: 640px;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
