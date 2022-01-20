<template>
  <div class="card">
   Titolo: {{info.title}} -
   Titolo Originale: {{ info.origina_title }} -
    Lingua:{{ info.language }} -
   Voto: {{ info.vote_average }} -
  </div>
</template>

<script>
export default {
name: 'Card',
 props: {
     info: Object,
},
};
</script>

<style>

</style>