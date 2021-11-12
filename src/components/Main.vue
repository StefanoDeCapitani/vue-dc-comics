<template>
  <main class="page__main">
    <div class="jumbotron"></div>
    <div class="container">
      <CardsGrid :cardsArray="cardsArray"></CardsGrid>
    </div>
  </main>
</template>

<script>
import JsonData from "@/assets/json/dc-comics.json";
import CardsGrid from "./CardsGrid.vue";

export default {
  name: "Main",
  components: {
    CardsGrid,
  },
  data() {
    return {
      cardsArray: JsonData,
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/styles/variables";

.page__main {
  background-color: black;
  color: white;
  padding-bottom: 2rem;
  .jumbotron {
    height: 400px;
    background-image: url("../assets/img/jumbotron.jpg");
    background-size: cover;
    background-position: top center;
  }
}
</style>
