<template>
  <div id="app">
      <img alt="Vue logo" src="./assets/Logo_vuejs.png">
      <div class="lien">
        <router-link to="/" id="link">Accueil</router-link> <!-- Activer la navigation utilisateur dans une app où le routeur est activé-->
        <router-link to="/films" id="link">Nos Films</router-link>
      </div>
      <h1 style="color: rgb(10,126,131); font-weight:bold;">IIM Streaming</h1>
      <router-view/> <!-- Permet fait le rendu des composants au dessus : https://router.vuejs.org/fr/api/#event-->
      <Footer/>
  </div>
</template>



<script>
import Vue from 'vue'
import { BootstrapVue, IconsPlugin} from 'bootstrap-vue'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

// Install BootstrapVue
Vue.use(BootstrapVue)
// Optionally install the BootstrapVue icon components plugin
Vue.use(IconsPlugin)

import Footer from'./components/Footer.vue'
export default {
  name: 'App',
  components: {
    Footer,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  background-color:#9c9a9a;
}

.lien{
  display: flex;
  width: 200px;
  justify-content: space-between;
  transform: translateY(-250px);
  margin-left: 1200px;
  font-size: 20px;
}

#link:hover{
  color: whitesmoke;
  text-decoration: none;

  cursor: pointer;
}


</style>

