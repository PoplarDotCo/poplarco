<template>
  <section id="hero">
    <div class="container">
      <div class="row direction_row">
        <div class="left-hero">
          <div class="image"></div>
          <img src="~/assets/img/kids-in-trash.png" alt="">
        </div>
        <div class="right-hero">
          <div class="content">
            <h1>What are we <span class="desktop-breakpoint"></span>leaving behind?</h1>
            <h4>We make it easy to clean up the mess we made</h4>
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

  .left-hero {
    width: 40%;

    img {
      max-width: 600px;
      width: 100%;
      border-radius: $borderRadius;
    }

  }

  .right-hero {
    width: 60%;
    //height: 100%;
    padding-left: 50px;
    //@include flex(column, nowrap, center, center);

    //h4 {
    //  margin-bottom: 40px;
    //}
  }

  //@include breakpoint(xs-down) {
  //  height: calc(100vh - 100px);
  //
  //  .row {
  //    @include flex(column);
  //
  //    .left-hero {
  //      height: 100px;
  //      width: 75%;
  //    }
  //
  //    .right-hero {
  //      padding: 30px 0;
  //      justify-content: flex-start;
  //    }
  //
  //  }
  //
  //}
}
</style>
