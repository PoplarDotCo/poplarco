<template>
  <section id="join-our-team" class="container">
    <div class="row direction_column">
      <h2>Join Our Team</h2>
      <p class="isH4">Check back often for spots on our growing team!</p>

      <div class="jobs" v-for="(job, index) in jobs" :key="index">
        <job :job="job.content"></job>
      </div>
    </div>
  </section>
</template>

<script>
import axios from 'axios';

import Job from '~/components/index/Job';

export default {
  name: "JoinOurTeam",
  components: { Job },
  data () {
    return {
      jobs: { content: {} }
    }
  },
  async mounted() {

    // TODO: Update so that his only pulls stories that are jobs
    await axios.get('https://api.storyblok.com/v2/cdn/stories?token=76Rkcs9ACYXy1OunSO1U6gtt')
    .then( (response) => {
      this.jobs = response.data.stories
    })

  },
}
</script>

<style lang="scss" scoped>
#join-our-team {


}
</style>
