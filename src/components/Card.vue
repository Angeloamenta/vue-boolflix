<template>
  <div class="card">
   Titolo: {{info.title}} -
   Titolo Originale: {{ info.original_title }} -
    Lingua:<country-flag :country='info.original_language' size='small'/>-
   Voto: {{ info.vote_average }} -
  </div>
</template>

<script>
import CountryFlag from 'vue-country-flag'
export default {
name: 'Card',
components: {
    CountryFlag,
},
 props: {
     info: Object,
},
};
</script>

<style>

</style>