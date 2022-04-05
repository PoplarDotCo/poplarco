<template>
  <div id="defaultLayout">
    <TopNav
      :items="nav"
    />
    <main>
      <router-view />
    </main>
    <MainFooter />
  </div>
</template>

<script>

export default {
  name: "DefaultLayout",
  data() {
    return {
      nav: [
        {
          url: '#what-we-do',
          text: 'What We Do'
        },
        {
          url: '#about-us',
          text: 'About'
        },
        {
          url: '#contact-us',
          text: 'Contact'
        },
        {
          url: '#join-our-team',
          text: 'Team'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
</style>
