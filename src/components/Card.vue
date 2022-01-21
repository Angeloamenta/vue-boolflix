<template>
  <div class="card">
    <div class="title">
   Titolo: {{titolo}}
    </div>
    <div class="original-title">
   Titolo Originale: {{ toriginale }}
    </div>
    <div class="languages">
    Lingua: <country-flag :country='lingua' size='small'/> {{lingua}}
    </div>
    <div class="vote">
   Voto:  {{  Math.floor(Math.round(voto / 2)) }} - <span v-for="n in Math.floor(Math.round(voto / 2))" :key="n"><i class="fas fa-star"></i></span>
    </div>
    <div class="img">
      <div v-if="img== null">Nessuna immagine Disponibile</div>
  <img v-else :src="`https://image.tmdb.org/t/p/w342/${img}`" alt="">
    </div>
  </div>
</template>

<script>
import CountryFlag from 'vue-country-flag';


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
    setRating:"2",
    }
},
created() {


},
};
</script>

<style lang="scss">
.card {
  display: flex;
  flex-direction: column;
  width: calc(100% / 5);
  text-align: center;
  
}
</style>>

