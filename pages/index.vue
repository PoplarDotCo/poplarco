<template>
  <div id="index">
    <top-nav></top-nav>
    <hero></hero>
    <what-we-do></what-we-do>
    <about-us></about-us>
    <contact-us></contact-us>
    <join-our-team></join-our-team>
    <main-footer></main-footer>
  </div>
</template>

<script>
import TopNav from "~/components/nav/TopNav";
import Hero from "~/components/index/Hero";
import AboutUs from "~/components/index/AboutUs";
import ContactUs from "~/components/index/ContactUs";
import JoinOurTeam from "~/components/index/JoinOurTeam";
import WhatWeDo from "~/components/index/WhatWeDo";
import MainFooter from "~/components/footer/MainFooter";

export default {
  name: "Index",
  components: {MainFooter, JoinOurTeam, ContactUs, AboutUs, WhatWeDo, Hero, TopNav}
}
</script>

<style lang="scss">
</style>
