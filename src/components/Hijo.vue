<template>

  <section class="src-components-hijo">
    <div class="jumbotron mt-3">
        <h1>Encriptador</h1>
        <h4>Palabra Recibida:</h4> {{ palabraRecibida }}
        <br>
        <br>
        <button 
            class="btn btn-success my-3"
            @click="encriptar()"
          > Encriptar {{ palabraRecibida }}
        </button>
    </div>
  </section>

</template>

<script lang="js">

  export default  {
    name: 'src-components-hijo',
    props: ['palabraRecibida'],
    mounted () {

    },
    data () {
      return {

      }
    },
    methods: {
      encriptar() {
        let temporal = ''
        var cursor = 0
        
        for (cursor = 0; cursor < this.palabraRecibida.length; cursor++)
        {
          //temporal = temporal + (this.palabraRecibida[cursor])
          temporal = temporal + String.fromCharCode((this.palabraRecibida.charCodeAt(cursor)) + 3)
        }

        temporal = temporal.split('').reverse().join('').toUpperCase()
        this.$emit('palabraSeEncripto',temporal )
      }

    },
    computed: {

    }
}


</script>

<style scoped lang="css">
  .src-components-hijo {

  }
</style>
