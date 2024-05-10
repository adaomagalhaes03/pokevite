<script setup>

const pokemon = defineProps(
    [
        "name", "urlbase"
    ]
)



</script>

<template>

    <div class=" col-4 ">
        <div class=" card p-2   cardList bg-info mb-3">
            <p class=" text-center ">{{ pokemon.name }}</p>
            <img :src="urlbase" height="80" class=" card-img-top" alt="">
            
        </div>
    </div>
   
</template>



<style  scoped>


.cardList{
    filter: grayscale(50%);
    transition: filter 0.3s ease, transform 0.3s ease;
    cursor: pointer; 
}

.cardList {
  position: relative; 
  overflow: hidden; 
}

.cardList img {
  transition: filter 0.3s ease, transform 0.3s ease, z-index 0.3s ease; 
}

.cardList img:hover {
  filter: blur(50%);
  filter: grayscale(0%);
  transform: scale(2.1);
  color: #fff !important;
  z-index: 1; 
}

.bg-info:hover{
    background-image: linear-gradient(45deg, rgba(187, 187, 187,0.04) 0%, rgba(187, 187, 187,0.04) 50%,rgba(86, 86, 86,0.04) 50%, rgba(86, 86, 86,0.04) 100%),linear-gradient(135deg, rgba(166, 166, 166,0.04) 0%, rgba(166, 166, 166,0.04) 50%,rgba(92, 92, 92,0.04) 50%, rgba(92, 92, 92,0.04) 100%),linear-gradient(90deg, rgb(20,20,20),rgb(20,20,20)); background-size: 142px 142px !important;
    color: #fff !important;
    /*background: #789aa2 !important;*/
}


</style>