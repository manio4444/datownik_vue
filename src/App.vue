<template>
  <div id="app">

    <MenuSidebar/>

    <StartPage msg="Welcome to Your Vue.js App"/>

  </div>
</template>

<script>
import MenuSidebar from './components/menu_sidebar.vue'
import StartPage from './components/start_page.vue'

export default {
  name: 'app',
  components: {
    StartPage,
    MenuSidebar,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
