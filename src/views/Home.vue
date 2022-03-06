<template>
  <v-app>
    <Navbar class="index" />
    <Dashboard />
    <Footer />
  </v-app>
</template>

<script>
import Dashboard from "../components/Dashboard.vue";
import Navbar from "../components/Navbar.vue";
import Footer from "../components/Footer.vue";

export default {
  name: "Home",

  components: {
    Dashboard,
    Navbar,
    Footer,
  },

  Navbar,
};
</script>

<style scoped>
.index {
  z-index: 999;
} 
</style>