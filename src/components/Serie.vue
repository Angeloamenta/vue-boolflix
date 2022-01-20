<template>
  <div class="series">
    Titolo: {{objinfo.name}} -
    Titolo Originale: {{ objinfo.original_name }} -
    Lingua:<country-flag :country='objinfo.original_language' size='small'/>-
    Voto: {{ objinfo.vote_average }} -
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
     objinfo: Object,
},
}
</script>

<style>

</style>