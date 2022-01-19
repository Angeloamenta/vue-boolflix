<template>
  <div id="app">
    <Header
    :filmSet="filmSel"
    @selectFilm="setFilm($event)"
    />
   <Main
   :testo="filmSel"

   />
    </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";

export default {
  name: "App",
  data() {
    return {
      filmSel:""
    }
  },
  components: {
    Header,
    Main,
  },
  computed: {
    
  },
  methods: {
    setFilm(value) {
      this.filmSel = value;
      console.log(value);
    },
  }
};
</script>

<style lang="scss">

</style>
