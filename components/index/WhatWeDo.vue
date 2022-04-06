<template>
  <section id="what-we-do">
    <div class="container">
      <div class="row direction_column">
        <h2>What we do</h2>
        <h4>Poplar aims to be your one stop shop for sustainable waste disposal</h4>
      </div>
      <div class="row direction_row cards">
        <GenericCard flex="2">
          <h3>Devices</h3>
          <p>Smart and thoughtful IoT consumer devices centered around sustainable waste management</p>
        </GenericCard>

        <div class="what-we-do__spacer"></div>

        <GenericCard flex="2">
          <h3>Services</h3>
          <p>Convenient and reliable services to aid you in your eco journey</p>
        </GenericCard>

        <div class="what-we-do__spacer"></div>

        <GenericCard flex="2">
          <h3>Rewards</h3>
          <p>Satisfying tracking, rewarding, and sharing tools to encourage you to be green</p>
        </GenericCard>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "WhatWeDo"
}
</script>

<style lang="scss">
#what-we-do {

  .cards {
    margin-top: 30px;

    .what-we-do__spacer {
      flex: 1;
    }

  }

}
</style>
