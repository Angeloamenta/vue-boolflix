<template>
  <div class="card">
   Titolo: {{titolo}} -
   Titolo Originale: {{ toriginale }} -
    Lingua: <country-flag :country='lingua' size='small'/> {{lingua}}-
   Voto:  {{  Math.round(voto) / 2 }} -
   <star-rating >2</star-rating>
  <star-rating @rating-selected="setRating"></star-rating>
  
  </div>
</template>

<script>
import CountryFlag from 'vue-country-flag';
import StarRating from 'vue-star-rating';


export default {
name: 'Card',
components: {
    CountryFlag,
    StarRating,
    
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

<style>

</style>