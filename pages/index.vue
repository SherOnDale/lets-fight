<template>
  <div class="container">
    <SearchBar @input="onSearch" />
    <Card
      v-for="item in filteredData"
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
  data() {
    return {
      searchTerm: ''
    }
  },
  computed: {
    filteredData() {
      if (this.searchTerm) {
        return this.data.filter((item) => {
          return item.content
            .toLowerCase()
            .trim()
            .includes(this.searchTerm.toLowerCase().trim())
        })
      }
      return this.data
    }
  },
  asyncData({ $axios }) {
    // const response = await $axios.get('https://api.myjson.com/bins/1d7hcy')
    const response = {}
    response.data = [
      {
        content: 'TEst one',
        twitterUrl: 'url one',
        youtubeUrl: 'url two'
      },
      {
        content: 'TEst one',
        twitterUrl: 'url one',
        youtubeUrl: 'url two'
      }
    ]
    return { data: response.data }
  },
  methods: {
    onSearch(value) {
      this.searchTerm = value
    }
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
