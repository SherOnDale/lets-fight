<template>
  <div class="searchbar__wrapper">
    <input @input="onInput" type="text" class="searchbar__input" />
  </div>
</template>

<script>
export default {
  methods: {
    onInput(event) {
      this.$emit('input', event.target.value)
    }
  }
}
</script>

<style scoped>
.searchbar__wrapper {
  border-bottom: 1px solid rgb(56, 68, 77);
  padding: 1rem;
  text-align: center;
}

.searchbar__wrapper input {
  padding: 0.5rem 1rem;
  width: 100%;
  max-width: 22.5rem;
  border-radius: 1rem;
}
</style>
