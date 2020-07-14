<template>

  <section class="src-components-padre">
    <div class="jumbotron mt-3">
        <h1>Ingreso de Datos</h1>
        <h4>Palabra: </h4>
        <input type="text" v-model="palabra"><br>
        <br>
        <h4>Palabra recibida:</h4> {{ palabra }}
        <br>
        <h4>Palabra encriptada:</h4> {{ palabraEncriptada }}
        <hr>
        <Hijo :palabraRecibida="palabra" @palabraSeEncripto="mostrarEncriptada($event)" />
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
