<template>
  <footer class="page__footer">
    <FooterNav />
    <SiteMap />
    <div class="sign-up-social">
      <div class="container sign-up-social__container">
        <a class="a btn--sign-up" href="#">Sign-Up Now!</a>
        <SocialLinks />
      </div>
    </div>
  </footer>
</template>

<script>
import FooterNav from "./FooterNav.vue";
import SiteMap from "./SiteMap.vue";
import SocialLinks from "./SocialLinks.vue";

export default {
  name: "Footer",
  components: {
    FooterNav,
    SiteMap,
    SocialLinks,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/styles/variables";

.sign-up-social {
  background-color: #303030;
  padding: $padding-30;
  .sign-up-social__container {
    display: flex;
    text-transform: uppercase;
    .btn--sign-up {
      border: 3px solid $color-primary;
      color: white;
      padding: 0.8rem;
    }
  }
}
</style>
