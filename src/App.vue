<template>
  <div id="app">
    <Navbar/>
    <router-view />
  </div>
</template>

<script>
import Navbar from '@/components/navbar/Navbar.vue'
export default {
  components: {
    Navbar
  }
};
</script>
