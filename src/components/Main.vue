<template>
  <header>
          <Card
          v-for="(film, index) in arrayff"
          :key="index"
          :titolo="film.title"
          :toriginale="film.original_title"
          :lingua="film.original_language"
          :voto="film.vote_average"
          />
          <Serie
          v-for="(serie, index) in arraySeries"
          :key="'A'+ index"
          :titolo="serie.name"
          :toriginale="serie.original_name"
          :lingua="serie.original_language"
          :voto="serie.vote_average"
          />  
  </header>
  
</template>

<script>
import Card from './Card.vue';
import Serie from './Serie.vue';



export default {
name: "Main",
components: {
     Card,
    Serie,
},
data() {
    return {
    
    }
},
props: {
   arrayff: {
       type: Array,
       default() {
           return [];
       },
   },
   arraySeries: {
       type: Array,
   },
  },
created() {


},
methods: {

}
}
</script>

<style>

</style>