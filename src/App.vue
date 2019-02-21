<template>
  <div id="app" :class="{reveal:true,bluesky:slide==5}" style="margin-top:0px;">
    <div class="slides">
      <section>
        <h1>Hello :)</h1>
      </section>
      <section>
        <h1>Just wanted to say..</h1>
      </section>
      <section>
        <h1>You a legend!</h1>
      </section>
      <section>
        <h1>And Super the best!</h1>
      </section>
      <section>
        <h1>And I'm super proud of you.</h1>
      </section>
      <section id="card">
        <h1>Happy Birthday!!!</h1>
        <img src="/HappyFathersDayScott/4DadHills.png">
      </section>
    </div>
  </div>
</template>

<script>

  import 'reveal/index.css'
  var Reveal = require('reveal/index');

  export default {
    name: 'App',
    components: {

    },
    mounted(){
      Reveal.initialize({
        width: 1080,
        height: 1920,
      })
      Reveal.addEventListener( 'slidechanged',( event ) => {
        this.slide = event.indexh;
      } );
    },
    watch:{

    },
    computed:{

    },
    data(){
      return {
        slide:0
      }
    }
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }

  .bluesky {
    /* Permalink - use to edit and share this gradient: http://colorzilla.com/gradient-editor/#56b1ea+0,60b7e0+100 */
    background: #56b1ea; /* Old browsers */
    background: -moz-linear-gradient(top, #56b1ea 0%, #60b7e0 100%); /* FF3.6-15 */
    background: -webkit-linear-gradient(top, #56b1ea 0%,#60b7e0 100%); /* Chrome10-25,Safari5.1-6 */
    background: linear-gradient(to bottom, #56b1ea 0%,#60b7e0 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
    filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#56b1ea', endColorstr='#60b7e0',GradientType=0 ); /* IE6-9 */
  }

  .bluesky h1{
    position: relative;
    color: white;
    font-weight: bolder;
    font-size: 10vh;
    top: -40vh;
    margin-top: 0px;
  }

  img {
    position: fixed;
    min-height: 150vh;
    min-width: 220vw;
    left:-40vh;
    top:-50vh;
  }

  h1{
    font-size: 7vh;
  }

</style>
