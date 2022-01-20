<template>
  <div class="card">
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
name: 'Card',
components: {
    CountryFlag,
},
//  props: {
//      info: Object,
// },
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
data() {
    return {
    flagsGb: "gb",
    }
},
created() {


},
};
</script>

<style>

</style>