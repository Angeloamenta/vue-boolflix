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
}
</script>

<style lang="scss">
header {
    background-color: black;
    height: 70px;
}
</style>>

