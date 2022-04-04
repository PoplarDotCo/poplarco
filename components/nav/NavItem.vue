<template>
  <a :href="item.url">
    {{ item.name }}
  </a>
</template>

<script>
export default {
  props: {
    item: {
      type: Array,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
nav {

}
</style>
