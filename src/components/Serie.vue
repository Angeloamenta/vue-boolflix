<template>
  <div class="series">
    Titolo: {{titolo}} -
    Titolo Originale: {{ toriginale }} -
    Lingua:<country-flag :country='lingua' size='small'/>-
    Voto: {{ voto }} -
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
},
}
</script>

<style>

</style>