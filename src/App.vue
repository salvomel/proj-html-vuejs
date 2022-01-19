<template>
  <div id="app">
    <Header :links = "navLinks" />
    <Main :cards = "cardList"/>
    <Footer :tweets= "tweetList" :contacts= "contactList"/>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
import data from './data/data.json'

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer
  },
  data: function () {
    return {
      navLinks: data.links,
      cardList: data.cards,
      tweetList: data.tweets,
      contactList: data.contacts
    }
  }
};
</script>

<style lang="scss">
  @import './style/general';
</style>
