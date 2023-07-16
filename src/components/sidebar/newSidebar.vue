<template>
  <div class="sidebar">
    <ul>
      <li v-for="item in menuItems" :key="item.id" @click="handleItemClick(item)">{{ item.label }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menuItems: [
        { id: 1, label: 'Dashboard', route: '/dashboard' },
        { id: 2, label: 'User Profile', route: '/userprofile' },
        { id: 3, label: 'Table List', route: '/tablelist' },
        { id: 4, label: 'File Manager', route: '/filemanager' },
        { id: 5, label: 'Contact', route: '/contact' }
      ]
    };
  },
  methods: {
    handleItemClick(item) {
      console.log('Clicked:', item.label);
    }
  }
};
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
  text-align: center;
  white-space: nowrap;
}

.sidebar li:hover {
  transform: scale(1.2);
}

@media (max-width: 768px) {
  .sidebar {
    width: 100%;
    height: auto;
    padding: 10px;
    margin-top: 1rem;
  }

  .sidebar ul {
    margin-top: 2rem;
  }

  .sidebar li {
    margin: 20px;
  }
}

@media (max-width: 576px) {
  .sidebar li {
    margin: 10px;
  }
}
</style>
