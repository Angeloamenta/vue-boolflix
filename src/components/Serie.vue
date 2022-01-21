<template>
  <div class="series">
    Titolo: {{titolo}} -
    Titolo Originale: {{ toriginale }} -
    Lingua:<country-flag :country='lingua' size='small'/>-
    Voto: {{  Math.round(voto) / 2 }} <span v-for="n in 5" :key="n"><i class="fas fa-star"></i></span> -
    <img :src="`https://image.tmdb.org/t/p/w342/${img}`" alt="">
  </div>
</template>

<script>
import CountryFlag from 'vue-country-flag'

export default {
  
name: 'Serie',
components: {
    CountryFlag,
},
props: {
  titolo: {
        type: String,
      },
      toriginale: {
        type: String,
      },
      lingua: {
        type: String,
      },
      voto: {
        type: Number,
      },
      img: {
        type: String,
        
      },
},
}
</script>

<style>

</style>