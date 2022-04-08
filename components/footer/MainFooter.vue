<template>
  <section id="footer">
    <div class="container">
      <div class="row direction_row">
        <div class="left">
          <img src="~/assets/img/logo_black.png" alt="Poplar Logo">
          <p>&copy; {{ getYear }} Poplar Labs, Inc.</p>
        </div>
        <div class="right">
          <p class="bold">Get In Touch</p>
          <p><a href="mailto:contact@poplar.co">contact@poplar.co</a></p>
          <p>(240)-801-7789</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MainFooter',
  props: {},
  method: {
    getYear () {
      console.log('test');
      // const date = new Date();
      // console.log(date.getFullYear());
      // return date.getFullYear();
    }
  }
}
</script>

<style lang="scss">
#footer {
  background: $colorMidGray;
  margin-top: 60px;

  .row {
    justify-content: space-between;
  }

  .left {
    img {
      width: 150px;
    }
    p {
      font-weight: $fontWeightMedium;
      margin-left: 8px;
    }
  }

  .right {

    .bold {
      font-weight: $fontWeightBold;
    }

    a,
    a:visited,
    a:focus,
    a:active {
      color: $black;
      text-decoration: underline;
    }
  }
}
</style>
