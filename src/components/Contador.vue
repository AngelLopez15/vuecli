<template>
  <h2>Tipo de cuenta: {{cuenta}}</h2>
  <h2>Saldo: {{saldo}}</h2>
  <h2>Cuenta: {{estado ? 'Activa' : 'Desactivada'}} </h2>
  <!-- Como no tenemos un id en el arreglo que vamos a recorrer 
  podemos ocupar el index de cada elemento del arreglo -->
  <div v-for="(servicio, index) in servicios" :key="index">
    {{ index + 1 }} - {{servicio}}
  </div>
  <!-- el nombre que va despues del @ es el que queramos -->
  <AccionSaldo 
    texto="Aumentar" 
    @accion="aumentar"
  />
  <AccionSaldo 
    texto="Disminuir" 
    @accion="disminuir"
    :desactivar='desactivar'
  />
  <AccionSaldo 
    texto="Resetear"
    @accion="resetear" 
  />
</template>

<script>
import AccionSaldo from './AccionSaldo'

export default {
  components:{
    AccionSaldo
  },
  data(){
    return{
      cuenta: 'Basica',
      saldo: 0,
      estado: true,
      servicios:['abono','pagos',' transferencia'],
      desactivar: false
    }
  },
  methods:{
    aumentar(){
      this.saldo=this.saldo+100
      this.desactivar=false
    },
    disminuir(){
      if (this.saldo===0) {
        this.desactivar=true
        return
      }
      this.saldo=this.saldo-100
    },
    resetear(){
      this.saldo=0
    }
  }
}
</script>

<style>

</style>