<template>
  <header>
      <div>
          <input v-model="nameFilm" type="text">
          <button @click="$emit('selectFilm', nameFilm)">premi</button>
      </div>
  </header>
</template>

<script>
export default {
name: "Header",
data() {
    return {
        nameFilm:"",
    }
},
methods: {

},
 props: {
     genres: {
       selectFilm: Function,
     },
 },
}
</script>

<style>

</style>