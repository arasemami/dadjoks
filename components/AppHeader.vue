<template>
  <header>
    <h1>Dad Jokes</h1>
    <ul>
      <li>
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/jokes">Jokes</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/about">About</nuxt-link>
      </li>
    </ul> 
  </header>
</template>

<script>
export default {
    name:'AppHeader'
};
</script>

<style  scoped>
header {
    display: flex;
    flex-direction: row;
    background-color: #efefef;
    width: 100%;
}
</style>