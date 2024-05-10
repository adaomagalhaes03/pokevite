<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HomeView from './views/HomeView.vue';
import TheCard from './views/TheCard.vue';

//importando referencias para seu usadas na varivaeis 
import { Fragment, ref } from 'vue';

let num =ref(0)



const nome = ref('Adam')


</script>

<template>
  
 
  
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
  <div class="container-fluid">
    <router-link class="navbar-brand" to="/">
    <img src="../src/assets/img/cube.png" width="30" class=" m-2" alt="">
       <strong>Pokevite 3.0</strong></router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <router-link class="nav-link active" aria-current="page" to="/">Home</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/about">About</router-link>
        </li>
       
      </ul>
    </div>
  </div>
</nav>
 
<!---content----->
   <div class=" main">
      <router-view></router-view>
   </div>


   <!--footer--->

   <footer class=" bg-primary text-light text-center">
    <div>
     
   Todos direitos reservados  |adamDev 🖥️ |  Ano {{ new Date().getFullYear() }}
   
    </div>
   </footer>

</template>

<style>

footer{
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  height:30px;

}

</style>
