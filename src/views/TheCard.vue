<script>

import { ref } from 'vue';

const name = ref("teste");

</script>


<template>
     <div class="card " >
  <img src="../assets/img/pokemon.png" class="card-img-top" alt="...">
  <div class="card-body">

    <h5 class=" card-text text-center">{{ teste }}</h5>
    <hr>
    <div class="row">
    <section class="col">
        <strong>XP:</strong>
        <span>100</span>
    </section>

    <section class="col">
        <strong>XP:</strong>
        <span>150</span>
    </section>
    </div>
  </div>
</div>
</template>



<style  scoped>

</style>