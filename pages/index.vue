<template>
  <div class="container">
    <SearchBar />
    <Card
      v-for="item in data"
      :content="item.content"
      :twitterUrl="item.twitterUrl"
      :youtubeUrl="item.youtubeUrl"
      :key="item._id"
    />
  </div>
</template>

<script>
import SearchBar from '~/components/SearchBar'
import Card from '~/components/Card'
export default {
  components: {
    SearchBar,
    Card
  },
  async asyncData({ $axios }) {
    const response = await $axios.get('https://api.myjson.com/bins/1d7hcy')
    return { data: response.data }
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
</style>
