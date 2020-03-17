<template>
  <div>
    <vs-navbar v-model="activeItem" class="nabarx" color="rgb(131, 97, 97)">
      <div slot="title">
        <img src="../assets/foto1.png" class="fotohome">
        <vs-navbar-title class="título"> Web Filmes </vs-navbar-title>
      </div>
      <vs-navbar-item index="0">
        <a href="http://localhost:8080/" class="complementos">Home</a>
      </vs-navbar-item>
      <vs-navbar-item index="1">
        <a href="#"  class="complementos">Filmes</a>
      </vs-navbar-item>
      <vs-navbar-item index="2">
        <a href="http://localhost:8080/"  class="complementos">Lançamentos</a>
      </vs-navbar-item>
      <vs-input class="pesquisa" icon="search" placeholder="Pesquisar Filmes" v-model="search"/>
    </vs-navbar>
  </div>

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
  // options here
})
export default {
  data:()=>({
    activeItem: 0,
    search: ''
  })
}
</script>

<style scoped>

    .fotohome{
      position: relative;
      size: 10px;
      width: 40px;
      left: 12px;
      top: 13px;

    }

    .título{
      position: relative;
      font-size: 25px;
      left: 57px;
      top: -20px;
      box-shadow: 5px 4px 3px black;
    }
    
    .pesquisa{
      position: relative;
      left: -8px;

    }

    .complementos{
      position: relative;
      left: -5px;
      font-size: 20px;
    }
  
</style>