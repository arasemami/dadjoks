<template>
  <nuxt-link :to="'jokes/' + joke.id">
    <div class="joke">
      <p>{{ joke.joke }}</p>
    </div>
  </nuxt-link>
</template>

<script>
export default {
  name: "Joke",
  props: {
    joke: Object,
  },
};
</script>

<style scoped>
.joke {
  padding: 1rem;
  border: 1px solid #303030;
  margin: 1rem;
}
</style>