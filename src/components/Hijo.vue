<template>

  <section class="src-components-hijo">
    <div class="jumbotron mt-3">
        <h1>Encriptador</h1>
        <h4>Palabra Encriptada</h4> <b> {{ this.encriptar | pasarAmayuscula }} </b>
        <br>
        <br>

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
      
    },
    computed: {
      encriptar() {
        let temporal = ''
        var cursor = 0
        
        for (cursor = 0; cursor < this.palabraRecibida.length; cursor++)
        {
          //temporal = temporal + (this.palabraRecibida[cursor])
          //temporal = temporal + String.fromCharCode((this.palabraRecibida.charCodeAt(cursor)) + 3)
          /*
          if ( this.palabraRecibida.charCodeAt(cursor) == 'a')
          {
            temporal = temporal + 'u'
          }
          if (this.palabraRecibida.charCodeAt(cursor) == 'e')
          {
            temporal = temporal + 'o'
          }
          if (this.palabraRecibida.charCodeAt(cursor) == 'o')
          {
            temporal = temporal + 'e'
          }
          if (this.palabraRecibida.charCodeAt(cursor) == 'u')
          {
            temporal = temporal + 'a'
          }
          */
         switch ( this.palabraRecibida[cursor] ) {
            case 'a':
                temporal = temporal + 'u';
                break;
            case 'e':
                temporal = temporal + 'u';
                break;
            case 'o':
                temporal = temporal + 'e';
                break;
            case 'u':
                temporal = temporal + 'a';
                break;
            default:
              temporal = temporal + this.palabraRecibida[cursor];
              break;

         }

        }

       
        return temporal
      }

    }
}


</script>

<style scoped lang="css">
  .src-components-hijo {

  }
</style>
