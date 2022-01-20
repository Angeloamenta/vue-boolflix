<template>
  <div class="series">
    Titolo: {{objinfo.name}} -
    Titolo Originale: {{ objinfo.origina_name }} -
    Lingua:{{ objinfo.original_language }} -
    Voto: {{ objinfo.vote_average }} -
  </div>
</template>

<script>
export default {
name: 'Serie',
props: {
     objinfo: Object,
},
}
</script>

<style>

</style>