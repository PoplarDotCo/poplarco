<template>
  <div class="generic-card" :style="cssStyles">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'GeneralCard',
  props: {
    backgroundColor: {
      default: '#dddddd',
      type: String,
      required: false,
    },
    borderRadius: {
      default: '5px',
      type: String,
      required: false,
    },
    flex: {
      default: '2',
      type: String,
      required: false
    }
  },
  computed: {
    cssStyles() {
      return {
        '--generic-card-background-color': this.backgroundColor,
        '--generic-card-border-radius': this.borderRadius,
        '--generic-card-flex': this.flex,
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.generic-card {
  background: var(--generic-card-background-color);
  border-radius: var(--generic-card-border-radius);
  flex: var(--generic-card-flex);
  padding: 30px;
}
</style>
