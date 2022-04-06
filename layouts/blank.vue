<template>
  <div class="container">
    <main>
      <router-view />
    </main>
  </div>
</template>

<script>
export default {
  name: 'BlankLayout',
}
</script>

<style lang="scss" scoped>
.container {
  padding: 100px 0;
}
</style>
