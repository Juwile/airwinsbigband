<template>
  <img alt="Logo AIRWIN's Big Band" class="logo" src="./assets/logo_abb.png">
  <a href="#/">Home3</a> |
  <a href="#/about">About</a> |
  <a href="#/non-existent-path">Broken Link</a>
  <div class="container">
    <component :is="currentView" />
  </div>
  
  
  
</template>

<script>
import Home from './components/Home.vue'
import About from './components/About.vue'
import NotFound from './components/NotFound.vue'

const routes = {
  '/': Home,
  '/about': About
}

export default {
  name: 'App',
  components: {
    Home,
    About
  },
  
  // Routing
  data() {
    return {
      currentPath: window.location.hash
    }
  },
  computed: {
    currentView() {
      return routes[this.currentPath.slice(1) || '/'] || NotFound
    }
  },
  mounted() {
    window.addEventListener('hashchange', () => {
		  this.currentPath = window.location.hash
		})
  }
}
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
  margin-top: 60px;
}

.container{
  display:grid;
  grid-template-columns: auto;
  margin:0 20% 0 20%;

}
.logo{
  width:300px;
    
  }

h1{
  color:#483016;
}
</style>    
