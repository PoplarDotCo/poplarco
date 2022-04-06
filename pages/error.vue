<template>
  <div class="container error-page">
    <p>404 Page Error</p>
    <h3>Sorry, looks like you got turned around there!</h3>
    <p><nuxt-link to="/">Click here to go home</nuxt-link></p>
  </div>
</template>

<script>
export default {
  name: 'Error',
  layout: 'blank'
}
</script>

<style lang="scss">
.error-page {
  padding: 100px 50px;
  .error-animation {
    width: 300px !important;
  }
}
</style>
