<template>
  <div class="footer__big-nav">
    <nav class="container">
      <ul class="nav__ul">
        <li class="nav__li" v-for="(link, i) in linksList" :key="i">
          <img
            class="nav__icon"
            :src="require('../assets/img/' + link.src)"
            :alt="link.text"
          />
          <a :href="link.href" class="nav__link">
            <p>{{ link.text }}</p>
          </a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "FooterNav",
  data() {
    return {
      linksList: [
        {
          src: "buy-comics-digital-comics.png",
          text: "digital comics",
          href: "#",
        },
        {
          src: "buy-comics-merchandise.png",
          text: "DC merchandise",
          href: "#",
        },
        {
          src: "buy-comics-subscriptions.png",
          text: "subscription",
          href: "#",
        },
        {
          src: "buy-comics-shop-locator.png",
          text: "comic shop locator",
          href: "#",
        },
        {
          src: "buy-dc-power-visa.svg",
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

  .nav__ul {
    display: flex;
    justify-content: space-around;
    gap: 2rem;
    margin: auto;
    .nav__li {
      display: flex;
      gap: 0.8rem;
      align-items: center;
      .nav__icon {
        height: 55px;
      }
      .nav__link {
        text-transform: uppercase;
        font-size: 0.8rem;
        color: white;
      }

      &:last-of-type {
        .nav__icon {
          height: 35px;
        }
      }
    }
  }
}
</style>
