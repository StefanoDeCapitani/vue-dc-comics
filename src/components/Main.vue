<template>
  <main class="page__main">
    <div class="container">
      <div class="cards-container">
        <Card
          v-for="(card, i) in cardsArray"
          :key="i"
          :thumbnail="card.thumb"
          :title="card.series"
        />
      </div>
    </div>
  </main>
</template>

<script>
import JsonData from "@/assets/json/dc-comics.json";
import Card from "./Card.vue";

export default {
  components: {
    Card,
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
  padding: $padding-50 0;
  .container {
    .cards-container {
      @include row(6, 0.5rem);
    }
  }
}
</style>
