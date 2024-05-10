<script setup>
  import { onMounted, ref, computed} from 'vue';
  import ListaPokems from '@/components/ListaPokems.vue';
  import TheCard from '@/views/TheCard.vue';

  let pokemons = ref([]);
  let urlbase = ref("https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/dream-world/");
  let Search = ref("")
  onMounted(() => {
    fetch("https://pokeapi.co/api/v2/pokemon?limit=100&offset=0")
      .then(res => res.json())
      .then(res => {
        pokemons.value = res.results;
      });
  });

  const pokemonsFilter = computed(() => {
  if (pokemons.value && Search.value) {
    return pokemons.value.filter(pokemon => {
      return pokemon.name.toLowerCase().includes(Search.value.toLowerCase());
    });
  }
  return pokemons.value;
});
//seleção de pokemons
const SelectedPokemons = (pokemon)=>{
   console.log(pokemon)
}

</script>

<template>
  <main>
    <div class="container mt-5 text-center">
  <div class="row flex">


    <div class="col col-sm-12   col-md-6  ">
     <the-card></the-card>

    </div>
    <div class="col col-sm-12 col-md-6 col">
     <div class="card">
      <div class="card-body   row">
        <div class="mb-3">
      <!--campo de busca filtrado-->
        <input  
        v-model="Search"
        type="text"
        id="Search"
         class="form-control"
          
            placeholder="pesquise...">
</div>
       <ListaPokems
        v-for="pokemon in pokemonsFilter"
        :key="pokemon.name"
        :name ="pokemon.name"
        :urlbase ="urlbase + pokemon.url.split('/')[6] + '.svg'"
        @clik="SelectedPokemons(pokemon)"
       />
      </div>
     </div>
    </div>
    
  </div>
</div>

  </main>
</template>

<style scoped>
p{
  text-align: justify;
   
}
</style>


