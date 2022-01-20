<template>
  <div class="series">
    Titolo: {{info.name}} -
    Titolo Originale: {{ info.origina_name }} -
    Lingua:{{ info.original_language }} -
    Voto: {{ info.vote_average }} -
  </div>
</template>

<script>
export default {
name: 'Serie',
props: {
     series: Object,
},
}
</script>

<style>

</style>