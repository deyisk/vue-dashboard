<template>
<div class="sidebar">
    <ul>
        <li v-for="item in menuItems" :key="item.id" @click="handleItemClick(item)">{{ item.label }}</li>
    </ul>
</div>
</template>

<script>
export default {
    data(){
        return{
            menuItems: [ //liste oluşturduk..
                { id:1, label:'Home', route: '/home'},
                { id:2, label: 'About', route: '/about'},
                { id:3, label: 'Services', route: '/services'},
                { id:4, label: 'Contact', route:'/contact'},
                { id:5, label:'Home', route: '/home'},
                { id:6, label: 'About', route: '/about'},
            ]
        };
    },
    methods:{
        handleItemClick(item){
            console.log('Clicked:',item.label)
        }
    }
}
</script>

<style>
.sidebar {
  background-color: #fecaca;
  width: 25vh;
  height: 100vh;
  padding: 10px;
}

.sidebar ul {
  list-style: none;
  padding: 5px;
  margin-top: 6rem;
}

.sidebar li {
  cursor: pointer;
  padding: 5px;
  margin: 50px;
}

.sidebar li:hover {
  background-color: #e0e0e0;
}
</style>


