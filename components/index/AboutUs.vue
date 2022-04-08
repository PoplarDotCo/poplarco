<template>
  <section id="about-us">
    <div class="container">
      <div class="row direction_row">
        <div class="div-left">
          <div class="content">
            <h2>About Us</h2>
            <p>Poplar trees are the first to take root after an environmental disaster. They grow fast and strong.</p>
            <p>Though they have a short lifespan (60 years), their life and death allow for more biodiverse plants and trees to re-enter the landscape.</p>
            <p>At Poplar, we aim to be like these pioneer trees.</p>
            <p>Poplar encourages waste reduction, mindset, and behavior changes through purposeful products and services.</p>
            <p>For decades, we have let waste degrade the spaces in which we work and play. But it's not too late to take root and begin the work of restoring our communities.</p>
            <p class="isH6">Each one of us can become pioneers.</p>
          </div>
        </div>
        <div class="div-right"></div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AboutUs"
}
</script>

<style lang="scss">
#about-us {
  width: 100%;

  .div-left {

    flex: 2;

    .content {
      max-width: 600px;
    }

  }

  .div-right {
    flex: 1;
    text-align: right;
    background: #fff url('~assets/img/compost.png') no-repeat top;
    background-size: cover;
    border-radius: $borderRadius;
  }

  @include breakpoint(xxs-down) {

    .direction_row {
      flex-direction: column-reverse;

      .div-right {
        flex: auto;
        height: 300px;
        width: 100%;
        background-position: center;
        margin-bottom: 30px;
      }

    }

  }

}
</style>
