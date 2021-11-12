<template>
  <div class="cards-container">
    <span class="section-label">CURRENT SERIES</span>
    <Card
      v-for="(card, i) in filteredArray"
      :key="i"
      :thumbnail="card.thumb"
      :title="card.series"
    />
    <button class="btn btn--load" @click="load()">
      {{ loadButtonMessage }}
    </button>
  </div>
</template>

<script>
import Card from "./Card.vue";

export default {
  name: "CardsGrid",
  components: {
    Card,
  },
  props: {
    cardsArray: Array,
  },
  data() {
    return {
      numberOfCardsToShow: 6,
      loadButtonMessage: "LOAD MORE",
    };
  },
  computed: {
    filteredArray: function () {
      let totalNumberOfCards = this.cardsArray.length;
      return this.numberOfCardsToShow < totalNumberOfCards
        ? this.cardsArray.slice(0, this.numberOfCardsToShow)
        : this.cardsArray;
    },
  },
  methods: {
    load() {
      let totalNumberOfCards = this.cardsArray.length;
      if (this.loadButtonMessage === "LOAD MORE") {
        if (this.numberOfCardsToShow + 6 <= totalNumberOfCards) {
          this.numberOfCardsToShow += 6;
        }
        if (this.numberOfCardsToShow === totalNumberOfCards) {
          this.loadButtonMessage = "SHOW LESS";
        }
      } else {
        this.loadButtonMessage = "LOAD MORE";
        this.numberOfCardsToShow = 6;
      }
    },
  },
};
</script>

<style scoped lang="scss">
@import "../assets/styles/variables";

.cards-container {
  position: relative;
  padding: $padding-50 0;
  @include cards-row(6, 0.5rem);

  .section-label {
    position: absolute;
    top: 0;
    transform: translate(-7%, -50%);
    background: $color-primary;
    padding: 0.7rem 1.5rem;
    font-weight: bold;
  }
  .btn--load {
    display: block;
    background: $color-primary;
    padding: 0.5rem 3rem;
    font-size: 0.8rem;
    margin: auto;
    position: relative;
    top: $padding-50;
    font-weight: bold;
  }
}
</style>
