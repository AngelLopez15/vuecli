<template>
  <button @click="accion" :disabled="desactivar">{{texto}}</button>
</template>

<script>
export default {
  name:'AccionSaldo',
  props:{
    // Como estamos pasando una props dinamica siempre es recomendable tener un valor por
    // default para los componentes que no usan alguna prop
    texto:String,
    desactivar:{
      type:Boolean,
      default:false
    }
  },
  // para ocupar el metodo que llega por props debemos declararlo en methods
  methods:{
    accion(){
      this.$emit('accion')
    }
  }
}
</script>

<style>

</style>