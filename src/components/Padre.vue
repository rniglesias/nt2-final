<template>

  <section class="src-components-padre">
    <div class="jumbotron mt-3">
        <h1>Ingreso de Datos</h1>
        <h4>Palabra Ingresada: </h4>
        <input type="text" v-model="palabra"><br>
        <br>
        
        <Hijo :palabraRecibida="palabra.toLowerCase()"/>
        <br>
    
        <h4>Multiple choice:</h4>
        1.- b
        <br>
        2.- b
        <br>
        3.- c
        <br>
        4.- b
        <br>
        5.- c
        <br>
    </div>
  </section>

</template>

<script lang="js">

  import Hijo from './Hijo.vue'

  export default  {
    name: 'src-components-padre',
    components : {
      Hijo
    },
    props: [],
    mounted () {

    },
    data () {
      return {
          palabra: '',
          palabraEncriptada: '',
      }
    },
    methods: {
      mostrarEncriptada(unapalabra) {
        this.palabraEncriptada = unapalabra
      }

    },
    computed: {

    }
}


</script>

<style scoped lang="css">
  .src-components-padre {

  }
</style>
