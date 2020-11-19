<template>
  <h1>{{texto}}</h1>
</template>

<script>
export default {
  // En name debemos poner el nombre del componente
  name:'Titulo',
  props:{
    texto:String
  }
}
</script>

<style scoped>
/* Al poner la palabra scoped estamos indicando a Vue que estos estilos solo aplican a este componente */
/* En estilos podemos trabajar como trabajamos CSS habitualmente */
  h1{
    color: cornflowerblue;
  }
</style>