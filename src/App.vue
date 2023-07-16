<template>
<div class="container">
  <router-view/>
  <new-navbar></new-navbar>
</div>
<div class="content">
  <new-sidebar></new-sidebar>
   <new-hero></new-hero>
</div>
</template>

<style>
.container {
  display: flex;
  flex-direction: column;
}

.content {
  flex: 1;
  display: flex;
  align-items: center;
  position:relative;
  margin-right:-100px;
}



@media (max-width: 768px) {
  .cards {
    width: 100%;
    margin-right: 0;
  }



}

@media (max-width: 576px) {
  .cards {
    margin-right: 20px;
  }
}

@media (max-width: 400px) {
  .cards {
    height: auto;
    padding: 20px;
  }
}


</style>

<script>
import newSidebar from "./components/sidebar/newSidebar.vue";
import newNavbar from "./components/navbar/newNavbar.vue";
import newHero from "./components/hero/newHero.vue";
export default {
  components:{
    
    newNavbar,
    newSidebar,
    newHero,
  }
  
}
</script>