<template>
  <main class="page__main">
    <div class="container">
      <p>--&gt; Content goes here &lt;--</p>
    </div>
  </main>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
@import "../assets/styles/variables";

.page__main {
  background-color: black;
  padding: $padding-50 0;
  .container {
    @include container-preset;
    p {
      color: white;
      font-size: 1.3rem;
    }
  }
}
</style>
