<template>
  <div class="job">
    <h5>{{ jobTitle }}</h5>
  </div>
</template>

<script>
export default {
  name: 'Job',
  props: {
    job: {
      type: Object,
      required: true,
    }
  },
  computed: {
    jobTitle() {
      return this.job && this.job && this.job.job_title;
    }
  }
}
</script>

<style lang="scss" scoped>
.job {
  background: $colorGrayShadow;
  border-radius: $borderRadius;
  padding: $cardPadding;
  margin: 30px 0;
}
</style>
