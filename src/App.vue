<template>
  <div id="app">
    <Header :links = "navLinks" />
    <Main />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
  },
  data: function () {
    return {
      navLinks: [
        {
          text: 'home',
          url: '#',
          current: true
        },
        {
          text: 'about',
          url: '#',
          current: false
        },
        {
          text: 'services',
          url: '#',
          current: false
        },
        {
          text: 'work',
          url: '#',
          current: false
        },
        {
          text: 'articles',
          url: '#',
          current: false
        },
      ],
    }
  },
};
</script>

<style lang="scss">
  @import './style/general';
</style>
