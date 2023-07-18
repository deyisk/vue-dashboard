<template>
  <div class="container">
    <div class="sidebar">
      <router-view/>
      <new-navbar></new-navbar>
      <new-sidebar></new-sidebar>
    </div>
    <div class="content">
      <new-hero></new-hero>
    </div>
  </div>
</template>
<style>
.container {
  height: 100%;
  display: flex;
}
.sidebar{
  margin-right:  100%;
}
.content{
  margin-top:50%;
  justify-content: space-between;
}
</style>
<script>
import newSidebar from "./components/sidebar/newSidebar.vue";
import newHero from "./components/hero/newHero.vue";
import NewNavbar from './components/navbar/newNavbar.vue';
export default {
  components: {
    newSidebar,
    newHero,
    NewNavbar,
  }
}
</script>
