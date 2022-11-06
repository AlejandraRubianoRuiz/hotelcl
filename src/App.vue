<template>
  <div>
    <router-view />
    <Sidebar></Sidebar>
  </div>
</template>

<script>
import Sidebar from './components/SidebarComponent.vue'

export default {
  components: {
    Sidebar,
  },
};
</script>

<style>
#app {
  font-family: "Akshar", Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #333;
  margin: 0;
  padding: 0;
}

body {
  background: #f8f8f8;
  box-sizing: border-box;
}

button {
  padding: 10px 25px !important;
  border-radius: 0 !important;
}

button:hover {
  box-shadow: 3px 3px 3px #777777;
}
</style>
