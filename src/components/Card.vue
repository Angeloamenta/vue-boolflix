<template>
  <div class="card">
    <div class="text">
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
   Voto:  {{  Math.floor(Math.round(voto / 2)) }} <span v-for="numero in Math.floor(Math.round(voto / 2))" :key="numero"><i class="fas fa-star"></i></span><span v-for="numeroDue in  5 -Math.floor(Math.round(voto / 2))" :key="'b' + numeroDue"><i class="far fa-star"></i></span>
    </div>
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
methods: {

}
};
</script>

<style lang="scss">
.card {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  width: calc(85% / 5 - 20px);
  height: 500px;
  margin-left: 20px;
  margin-top: 20px;
  text-align: center;
  background-color: black;
  color: white;
  border: 2px solid white;
  position: relative;
  overflow: hidden;
  &:active .img,
  &:hover .img,
  &:focus .img{
    display: none;
  }
  .img {
    width: 100%;
    height: 100%;
    position: absolute;
    transform: translate(-50%, -50%);
    top: 50%;
    left: 50%;    
    
  }

  .fa-star {
    color: yellow;

    
  }
}
</style>

