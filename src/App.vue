<template>
  <router-view/>
  <new-navbar></new-navbar>
  <new-sidebar></new-sidebar>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>

<script>
import newSidebar from "./components/sidebar/newSidebar.vue";
import newNavbar from "./components/navbar/newNavbar.vue";
export default {
  components:{
    newSidebar,
    newNavbar
  }
  
}
</script>