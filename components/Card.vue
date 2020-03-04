<template>
  <div class="card__wrapper">
    <p>{{ content }}</p>
    <p>{{ twitterUrl }}</p>
    <p>{{ youtubeUrl }}</p>
  </div>
</template>

<script>
export default {
  props: {
    content: {
      type: String,
      default: ''
    },
    twitterUrl: {
      type: String,
      default: 'https://www.twitter.com'
    },
    youtubeUrl: {
      type: String,
      default: 'https://www.youtube.com'
    }
  }
}
</script>

<style scoped>
.card__wrapper {
  border-bottom: 1px solid rgb(56, 68, 77);
}
</style>
