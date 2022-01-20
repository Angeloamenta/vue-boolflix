<template>
  <div class="series">
    Titolo: {{titolo}} -
    Titolo Originale: {{ toriginale }} -
    Lingua:<country-flag :country='lingua' size='small'/>-
    Voto: {{ voto }} -
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