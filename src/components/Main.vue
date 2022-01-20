<template>
  <header>
          <Card
          v-for="(film, index) in arrayff"
          :key="index"
          :info="film"
          />
          <Serie
          v-for="(serie, index) in arraySeries"
          :key="'A'+ index"
          :objinfo="serie"
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
//  axios.get(`${this.query}${this.nameFilm}${this.query2}`)
//     .then((result) => {
//         console.log(result.data);
//         this.arrayFilm = result.data.results,
//         console.log("array", this.arrayFilm);
//         this.nameFilm = this.testo;
//         console.log("nome", this.namefilm);
//         // this.$emit('ricerca', this.nameFilm);
        
//     })
//     .catch((error) => {
//         console.log(error);
//     })
    
},
methods: {
// richiamo() {
//     axios.get(`${this.query}${this.testo}${this.query2}`)
//         .then((result) => {
//             this.arrayFilm = result.data.results, 
//             this.nameFilm = this.testo;           
//         })
//         .catch((error) => {
//             console.log(error);
//         })
// //  this.$emit('ricerca', this.nameFilm);
// // console.log(this.$emit);
// // console.log(this);
// }
}
}
</script>

<style>

</style>