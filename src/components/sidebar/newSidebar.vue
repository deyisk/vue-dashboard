<template>
  <div class="sidebar">
    <ul>
      <li
        v-for="item in menuItems"
        :key="item.id"
        @click="handleItemClick(item)"
      >
        {{ item.label }}
      </li>
    </ul>
  </div>
 
</template>


<script>
export default {
  data() {
    return {
      menuItems: [
        { id: 1, label: "Dashboard", route: "/dashboard" },
        { id: 2, label: "User Profile", route: "/userprofile" },
        { id: 3, label: "Table List", route: "/tablelist" },
        { id: 4, label: "File Manager", route: "/filemanager" },
        { id: 5, label: "Contact", route: "/contact" },
      ],
    };
  },
  methods: {
    handleItemClick(item) {
      console.log("Clicked:", item.label);
    },
  },
};
</script>

<style>

#app{
  height: 100%;
   margin-top: 0;
  padding-top: 0;
   margin: 0;
}

body{
  margin:0;
  margin-top:0;
}

html,body{
  height: 100%;
  width: 50%;
  background-color: pink;
  margin: 0;
  margin-top: 0;
  padding-top: 0;
}

.sidebar{
  height: 100%;
  width:50%;
  max-width: 250px;
  min-width: 180px;
  background-color: red;
  margin: 0;
  padding: 0;
  margin-top: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  overflow:hidden;

}

.sidebar ul{
  list-style:none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  
  
}

.sidebar li{
  cursor:pointer;
  text-align: center;
  margin-bottom:25%;
}

.sidebar li:hover{
  transform: scale(1.2);
}


</style>
