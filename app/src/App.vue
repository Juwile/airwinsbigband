<template>
  <img alt="Logo AIRWIN's Big Band" class="logo" src="./assets/logo_abb.png">
  <div class="container">
    <Home/>
  </div>
  
</template>

<script>
import Home from './components/Home.vue'

export default {
  name: 'App',
  components: {
    Home
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
