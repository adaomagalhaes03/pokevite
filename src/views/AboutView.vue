<script>
import { ref } from 'vue';

export default {
  setup() {
    const Name = ref('Adão Magalhães')
    const age = ref(21)

    return { Name, age };
  }
}

</script>

<template>
  <div class=" container mt-5">
  <h2>Sobre o <strong>Pokevite</strong></h2>

  <p>
  
    O vídeojogo Pokémon, uma das franquias globais mais bem sucedidas, assinalou, no dia 27 de fevereiro, os 25 anos da estreia no Japão, agora reforçado pela pandemia da covid-19 que tem impulsionado o entretenimento digital.

Neste mesmo dia, em 1996, os títulos originais da franquia, "Pokémon Red" e "Pokémon Green", foram lançados no Japão para o não menos revolucionário Game Boy da Nintendo, no qual o jogador desempenhava o papel de um rapaz que sonha apanhar todos os "Pocket Monsters", ou na abreviatura, pokémon.

Um quarto de século mais tarde, esses títulos e 150 criaturas evoluíram, em formato e género, para a publicação de dezenas de jogos que venderam mais de 368 milhões de cópias, com mais de 800 pokémon para descobrir, catalogar e reproduzir.
  </p>

  <p>
    desenvolvido por <strong> {{ Name }}</strong>,  {{ age }} Anos de idade!
  </p>
  </div>
</template>
<style>

</style>
