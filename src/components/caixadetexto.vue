<template lang="html">
<vs-row vs-w="12">
    <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-lg="2" vs-sm="4" vs-xs="12" >
    <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-lg="8" vs-sm="4" vs-xs="12">
    <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-lg="2" vs-sm="4" vs-xs="12">
  <div class="centerx">
    <vs-button @click="popupActivo=true" color="danger" type="gradient" icon="favorite">+ sobre</vs-button>
    <vs-popup class="holamundo"  title="Fight Club" :active.sync="popupActivo" color="rgb(131, 97, 97)">
      <p class="sinopse" >Um homem deprimido que sofre de insônia conhece um estranho vendedor chamado Tyler Durden e se vê morando em uma casa suja depois que seu perfeito apartamento é destruído.<br>A dupla forma um clube com regras rígidas onde homens lutam. A parceria perfeita é comprometida quando uma mulher, Marla, atrai a atenção de Tyler. <br><br><br>
          <p class="sinopse1" >Data de lançamento: 29 de outubro de 1999 (Brasil) <br> Direção: David Fincher
          Autor: Chuck Palahniuk<br>
          Bilheteria: 100,9 milhões USD</p>
        <br><br>
        <a href="https://www.youtube.com/watch?v=B6RdzLkQ-bY" class="link">Trailer Oficial</a>
        <a href="https://www.foxmovies.com/movies/fight-club" class="link2">/ Fox Filmes</a>

        <img class="img" src="https://image.tmdb.org/t/p/w500//4GpwvwDjgwiShr1UBJIn5fk1gwT.jpg" width="40%"> 
        <img class="pictures" src="https://image.tmdb.org/t/p/w500//tEiIH5QesdheJmDAqQwvtN60727.png" width="6%"> 
        <img class="pictures2" src="https://image.tmdb.org/t/p/w500//hD8yEGUBlHOcfHYbujp71vD8gZp.png" width="6%"> 
        <img class="pictures3" src="https://image.tmdb.org/t/p/w500//7PzJdsLGlR7oW4J0J5Xcd0pHGRg.png" width="7%">         
     </vs-popup>
  </div>
    </vs-col>
    </vs-col>
    </vs-col>
</vs-row>
</template>

<script>
import Vue from 'vue'
import Vuesax from 'vuesax'
import 'material-icons/iconfont/material-icons.css';

import 'vuesax/dist/vuesax.css' //Vuesax styles
Vue.use(Vuesax, {
      theme:{
    colors:{
      primary:'#5b3cc4',
      success:'rgb(23, 201, 100)',
      danger:'rgb(242, 19, 93)',
      warning:'rgb(255, 130, 0)',
      dark:'rgb(36, 33, 69)'
    }
  }
})

export default {
  data(){
    return {
      popupActivo:false,
    }
  }
}
</script>

<style scoped>

    .centerx{
    position: absolute;
    position:relative;
    text-align:center;
    position:absolute;
    z-index:1;
    top:68%;
    left: 74%;
    width:60px;               
    height:30px;              
    padding:0;
    margin:-15px 0 0 -30px;   
    border:0 none;
    }
    .sinopse1{
      position: relative;
      font-weight: bold;  
    }
    .pictures2{
      position: relative;
      left: 3%;

    }
    .pictures{
      position: relative;
      left: 2%;
    }
    .pictures3{
      position: relative;
      left: 4%;

    }
    .link{
      position: relative;
      top: -350px;
    }
     .link2{
      position: relative;
      top: -350px;
      left: 5px;
    }
    .img {
      overflow: hidden;
      max-width: 100%;
      -moz-transition: all 0.3s;
      -webkit-transition: all 0.3s;
      transition: all 0.3s;
    }

    .img:hover {
      -moz-transform: scale(1.1);
      -webkit-transform: scale(1.1);
      transform: scale(1.1);
    }

</style>