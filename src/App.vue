<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!-- <HelloWorld msg="Bienvenido a Vue.js App con CLI"/> -->
  <!-- Para renderizar los elementos en el DOM debemos de importar el componente
  dentro de template -->
  <!-- Enviando props dinamicos -->
  <Titulo texto="Mi banco dinamico 2.0 con Cli de Vue 3"/>
  <Contador />
</template>

<script>

// Para poder usar nuestros componentes .vue debemos de importarlos
// Es importante que los importemos antes del export default y dentro de script
// import HelloWorld from './components/HelloWorld.vue'

import Titulo from './components/Titulo'
import Contador from './components/Contador'

export default {
  name: 'App',
  components: {
    // HelloWorlds
    Titulo,
    Contador
  }
}
</script>

<style>
/* Los styles son optativos */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
