<template>
  <div class="container">
    <nav>
      <div class="left-nav">
        <nuxt-link to="/" aria-label="Home" title="home">
          <img src="~/assets/img/logo_black.png" alt="Poplar Logo">
        </nuxt-link>
      </div>

      <div class="right-nav" :class="navClosed ? '' : 'open'">
        <div class="nav-item" v-for="(item, index) in items" :key="index">
          <a class="nav-item__link" :href="item.url">{{ item.text }}</a>
        </div>
      </div>

      <div class="hamburger" :class="navClosed ? 'closed' : 'open'" @click="toggleNav">
        <div class="top-bun"></div>
        <div class="meat"></div>
        <div class="bottom-bun"></div>
      </div>

    </nav>
  </div>
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
      required: true
    }
  },
  data() {
    return {
      navClosed: true,
    }
  },
  methods: {
    toggleNav() {
      this.navClosed = !this.navClosed;
      this.freezeUnfreezeBody();
    },
    freezeUnfreezeBody() {
      if(this.navClosed) {
        document.getElementById('poplar').remove('no-scroll');
      }

      if (!this.navClosed) {
        document.getElementById('poplar').add('no-scroll');
      }
    },
    spin(times_spun) {
      // do something using times_spun
    },
    jumpingjack() {},
    jump(distance, times_spun) {
      // use distance for jump dist

      this.spin(times_spun)
      this.jumpingjack()
    }
  }
}
</script>

<style lang="scss" scoped>
nav {
  display: flex;
  @include flex(row, nowrap, space-between);

  padding: 20px 0;
  background: $white;
  position: relative;

  .left-nav {


    a, a:visited {
      border: none;
    }

    img {
      height: 30px;
    }

  }

  .right-nav {
    @include flex(row, nowrap, flex-end);

    .nav-item {
      margin-left: 20px;

      &__link,
      &__link:visited {
        color: black;
      }

      a:hover {
        opacity: 0.75;
      }

    }

  }

  .hamburger {
    cursor: pointer;
    position: absolute;
    right: 20px;
    top: 20px;

    div {
      background: $black;
      width: 30px;
      height: 5px;
      border-radius: 30%;
      margin-bottom: 3px;
      transition: all .3s ease-in;
    }

    &.open {

      .meat {
        display: none;
        transition: all .3s ease-in;
      }

      .top-bun {
        transform: rotate(45deg);
        transition: all .3s ease-in;
        margin-bottom: -5px;
      }

      .bottom-bun {
        transform: rotate(-45deg);
        transition: all .3s ease-in;
      }

    }

    @include breakpoint(sm-up) {

      display: none;

    }

  }

}

@include breakpoint(xs-down) {

  .container {
    padding: 0;
  }

  nav {
    @include flex(column, nowrap, space-between, flex-start);

    .left-nav {
      width: 100%;
      text-align: center;
    }

    .right-nav {
      @include flex(column, nowrap, flex-start);
      width: 100vw;
      height: 100vh;
      background: white;
      padding-top: 100px;
      display: none;

      .nav-item {
        width: 100%;
        text-align: center;
        margin: 20px 0 50px;
        font-size: 1.5rem;

        &__link,
        &__link:visited {
          text-decoration: underline;
        }

      }

      &.open {
        display: block;
        transition: $transitionIn;
      }

    }
  }

}

</style>

<style>
.no-scroll {
  overflow: hidden;
}
</style>
