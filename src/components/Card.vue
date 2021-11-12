<template>
  <div class="card">
    <div class="ratio">
      <div class="content">
        <img class="card__img" :src="thumbnail" alt="" />
      </div>
    </div>
    <p class="card__text">{{ title }}</p>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    thumbnail: String,
    title: String,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/styles/variables";

.card {
  padding: 1rem 0;
  @include ratio(100%);
  .card__img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: top;
  }
  .card__text {
    text-transform: uppercase;
    font-size: 0.8rem;
  }
}
</style>
