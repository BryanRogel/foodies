<template>
  <div class="home">
    <LandingHome />
    <LandingContact />
    <img alt="Vue logo" src="../assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
// @ is an alias to /src
import LandingHome from '@/components/landingPage/LandingHome.vue'
import LandingContact from '@/components/landingPage/LandingContact.vue'
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    // HelloWorld,
    LandingHome,
    LandingContact
  }
}
</script>
