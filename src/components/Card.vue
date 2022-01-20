<template>
  <div class="card">
   Titolo: {{info.title}} -
   Titolo Originale: {{ info.original_title }} -
    Lingua:{{ info.original_language }} -
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