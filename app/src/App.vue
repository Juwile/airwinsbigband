<template>
  <header>
    <nav>
      <a href="#/">Home</a> |
      <a href="#/about">About</a> |
      <a href="#/non-existent-path">Broken Link</a>
    </nav>
    <a class="logo-container" href="#/"><img alt="Logo AIRWIN's Big Band" class="logo" src="./assets/logo_abb.png" ></a>
  </header>
  <div class="container">
    <component :is="currentView" />
  </div>
</template>

<script>
import HomeComponent from './components/HomeComponent.vue'
import AboutComponent from './components/AboutComponent.vue'
import NotFound from './components/NotFound.vue'

const routes = {
  '/': HomeComponent,
  '/about': AboutComponent
}

export default {
  name: 'App',
  components: {
    HomeComponent,
    AboutComponent
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
@import url('https://fonts.googleapis.com/css2?family=Shadows+Into+Light+Two&display=swap');

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: black;
}

header{
  padding-top: 1em;
  padding-bottom: 2em;
  display: grid;
  grid-template-columns: 2;

}

nav{
  grid-column: 1 / 2;
  display: flex;
  justify-content: flex-start;
  font-size: 1.2em;
  font-family: 'Shadows Into Light Two', cursive;

}

a{
  padding-right: 1em;
  padding-left: 1em;
  text-decoration: none;
  color:#483016;
  


}

a:link{
  color:#483016;
  
}
a:visited{
  color:#483016;
}

a:hover{
  color:red;
}

a:active{
  color:blue;
}

.logo{
  width:200px;
  
  }

  .logo-container{
    grid-column: 2 / 2;
    display: flex;
    justify-self: flex-end;
    margin-right: 1em;
  }

.container{
  display:grid;
  grid-template-columns: auto;
  margin:0 10% 0 10%;

}

h1,h2{
  color:#483016;
  font-family: 'Shadows Into Light Two', cursive;
}

h2{
  text-align: left;
}

p{
  font-size: 1.2em;
}
</style>    
