<template>
  <footer class="page__footer">
    <FooterNav />
    <div class="site-map">
      <ul></ul>
    </div>
  </footer>
</template>

<script>
import FooterNav from "./FooterNav.vue";

export default {
  name: "Footer",
  components: {
    FooterNav,
  },
  data() {
    return {};
  },
};
</script>

<style></style>
