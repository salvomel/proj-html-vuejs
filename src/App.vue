<template>
  <div id="app">
    <Header :links = "navLinks" />
    <Main :cards = "cardList"/>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import data from './data/data.json'

export default {
  name: "App",
  components: {
    Header,
    Main,
  },
  data: function () {
    return {
      navLinks: data.links,
      cardList: data.cards
    }
  },
};
</script>

<style lang="scss">
  @import './style/general';
</style>
