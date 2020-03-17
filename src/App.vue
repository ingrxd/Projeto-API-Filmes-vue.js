<template>
  <div id="app">
    <navbar/>
    <caixadetexto/>
      <div class="container body-content">
       @RenderBody()
        <footer class="fixarRodape footer">
        <hr>
        <p>&copy; @Foxmovies.com.br</p>
        </footer> 
        <iframe class="video" width="370" height="300" src="https://www.youtube.com/embed/ejvK2jW8dh8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        <div class="texthome"> Um homem deprimido que sofre de insônia conhece um<br> estranho vendedor chamado Tyler<br> Durden e se vê morando em uma casa suja depois que<br> seu perfeito apartamento é destruído. A dupla forma um clube com regras rígidas onde homens lutam. A parceria perfeita é comprometida <br>quando uma mulher, Marla, atrai a atenção de Tyler.<br><br>Popularidade: 31.636 </div>
        <img class="capahome" src="./assets/capahome2.png">
                      {{ info }}
      </div>
  </div>
</template>

<script>
import navbar from './components/navbar.vue';
import caixadetexto from './components/caixadetexto.vue';
import axios from 'axios';


axios.get('https://api.themoviedb.org/3/movie/550?api_key=c341e275f3a5189bbd9509ee1063cb5b')
.then(response => this.info = response.data)
.catch(error => console.log(error))

export default {
  name: 'App',
  components: { navbar, caixadetexto },
  data () {
    
    return {
      info: null
    }
  },  
}
</script>

<style scoped>
    
    .texthome{
      color: teal;
      font-size: 150%;
      position: absolute;
      margin-top: -2%;
      padding-top: 20% ;
      padding-left: 60%;
      z-index: 1;
      color: white; text-shadow: black 0.1em 0.1em 0.2em;
      text-shadow: #000 2px 3px 2px;
    }
    .fixarRodape {
        bottom: 0;
        position: fixed;
        width: 100%;
        text-align: center;
    }
    .footer {
        position: fixed;
        left: 0;
        bottom: 0;
        width: 100%;
        background-color: rgb(39, 38, 38);
        color: white;
        text-align: center;
    }
    .capahome{
       position: relative;
       width: 100%;
       height: 100%;
       top: 2px;

    }
    .video{
      position: absolute;
      padding-top: 2%;
      margin-top: 2%;
      margin-left: 72%;
      z-index: 1;

    }
    #app{
      background-color: rgb(0, 0, 0);

    }
</style>

  
