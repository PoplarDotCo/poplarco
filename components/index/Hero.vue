<template>
  <section id="hero">
    <div class="container">
      <div class="row direction_row">
        <div class="left-hero"></div>
        <div class="right-hero">
          <div class="content">
            <h1>What are we <span class="desktop-breakpoint"></span>leaving behind?</h1>
            <p class="isH4">We make it easy to clean up the mess we made</p>
            <a href="#contact-us" class="button button_lg">Request More Info</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "IndexHero"
}
</script>

<style lang="scss">
#hero {

  .row {


  }

  .left-hero {
    width: 40%;
    background: #fff url('~assets/img/kids-in-trash.png') no-repeat top center;
    background-size: cover;
    border-radius: $borderRadius;

  }

  .right-hero {
    width: 60%;
    padding: 50px;
  }

  @include breakpoint(xxs-down) {

    .direction_row {
      flex-direction: column;
    }

  }

}
</style>
