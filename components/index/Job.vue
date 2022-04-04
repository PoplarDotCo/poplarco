<template>
  <div class="job">
    <h5>{{ title }}</h5>
    <p>
      <span>{{ type }}</span>&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;<span>{{ location }}</span>
    </p>

    <div class="desc">
      <p>{{ description }}</p>
    </div>

    <div class="links">
      <h6>Learn More:</h6>

      <div class="row direction_row">
        <a :href="linkedIn" class="button button_sm" target="_blank" v-if="linkedIn">LinkedIn</a>
        <a :href="angelList" class="button button_sm" target="_blank" v-if="angelList">Angel List</a>
      </div>
    </div>
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
    title() {
      return this.job && this.job.job_title;
    },
    type() {
      return this.job && this.job.job_type;
    },
    location() {
      return this.job && this.job.job_location;
    },
    description() {
      return this.job && this.job.job_description;
    },
    linkedIn() {
      return this.job && this.job.job_linkedin_link && this.job.job_linkedin_link.url;
    },
    angelList() {
      return this.job && this.job.job_angel_list_link && this.job.job_angel_list_link.url;
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

  h5 {
    margin-bottom: 0;
  }

  h6 {
    margin-top: 30px;
  }

  a {
    margin: 20px 30px 0 0;
  }

}
</style>
