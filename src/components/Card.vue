<template>
  <div class="card">
   Titolo: {{titolo}} -
   Titolo Originale: {{ toriginale }} -
    Lingua:<country-flag :country='lingua' size='small'/>-
   Voto: {{ voto }} -
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