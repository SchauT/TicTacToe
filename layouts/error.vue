<template>
  <div class="container">
    <h1 v-if="error.statusCode === 404">404 Page not found</h1>
    <h1 v-else>An error occurred</h1>
    <div>
      <NuxtLink to="/" class="button">Home page</NuxtLink>
    </div>
  </div>
</template>

<script>
export default {
  props: ['error'],
  layout: 'blog' // you can set a custom layout for the error page
}
</script>

<style scoped>
.container {
	margin: 0 auto;
	height: 80vh;
	display: flex;
	padding-top: 60px;
}
.button {
  margin: 20px;
}
</style>