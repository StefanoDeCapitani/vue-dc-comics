<template>
  <div id="app">
    <Header :currentLink="currentLink" />
    <Main> </Main>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
  data() {
    return { currentLink: 1 };
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap");
@import "assets/styles/variables";
@import "assets/styles/utilities";

#app {
  font-family: "Roboto", sans-serif;
}
</style>
