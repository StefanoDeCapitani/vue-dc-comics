<template>
  <div class="footer__big-nav">
    <nav class="container">
      <img src="../assets/img/buy-comics-digital-comics.png" alt="" />
      <ul class="nav__ul">
        <li class="nav__li" v-for="(link, i) in linksList" :key="i">
          <img :src="link.src" :alt="link.text" />
          <a :href="link.href">
            <p>{{ link.text }}</p>
          </a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "FooterBigNav",
  data() {
    return {
      linksList: [
        {
          src: "assets/img/buy-comics-digital-comics.png",
          text: "digital comics",
          href: "#",
        },
        {
          src: "../assets/img/buy-comics-merchandise.png",
          text: "DC merchandise",
          href: "#",
        },
        {
          src: "../assets/img/buy-comics-subscriptions.png",
          text: "subscription",
          href: "#",
        },
        {
          src: "../assets/img/buy-comics-shop-locator.png",
          text: "comic shop locator",
          href: "#",
        },
        {
          src: "../assets/img/buy-comics-power-visa.svg",
          text: "DC power visa",
          href: "#",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/styles/variables";
.footer__big-nav {
  background-color: $color-primary;
  padding: $padding-50 0;
}
</style>
