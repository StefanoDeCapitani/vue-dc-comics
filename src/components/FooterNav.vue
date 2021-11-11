<template>
  <div class="footer__big-nav">
    <nav class="container">
      <ul class="nav__ul">
        <li class="nav__li" v-for="(link, i) in linksList" :key="i">
          <a :href="link.href" class="nav__link">
            <img
              class="nav__icon"
              :src="require('../assets/img/' + link.src)"
              :alt="link.text"
            />
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
    align-items: center;
    gap: 2rem;
    margin: auto;
    .nav__li {
      .nav__link {
        display: flex;
        gap: 1rem;
        align-items: center;
        text-transform: uppercase;
        font-size: 0.8rem;
        color: white;
        .nav__icon {
          height: 55px;
        }
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
