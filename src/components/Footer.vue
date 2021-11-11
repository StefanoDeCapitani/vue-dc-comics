<template>
  <footer class="page__footer">
    <FooterNav />
    <SiteMap />
    <div class="sign-up-social">
      <div class="container sign-up-social__container">
        <a class="btn--sign-up" href="#">Sign-Up Now!</a>
        <div class="social">
          <h3>Follow us</h3>
          <ul>
            <li v-for="(social, i) in socialList" :key="i">
              <a :href="social.href">
                <img
                  :src="require('../assets/img/' + social.src)"
                  :alt="social.alt"
                />
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import FooterNav from "./FooterNav.vue";
import SiteMap from "./SiteMap.vue";

export default {
  name: "Footer",
  components: {
    FooterNav,
    SiteMap,
  },
  data() {
    return {
      socialList: [
        {
          src: "footer-facebook.png",
          alt: "Facebook",
          href: "#",
        },
        {
          src: "footer-twitter.png",
          alt: "Twitter",
          href: "#",
        },
        {
          src: "footer-youtube.png",
          alt: "YouTube",
          href: "#",
        },
        {
          src: "footer-pinterest.png",
          alt: "Pinterest",
          href: "#",
        },
        {
          src: "footer-periscope.png",
          alt: "Periscope",
          href: "#",
        },
      ],
    };
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
    .social {
      margin-left: auto;
      display: flex;
      align-items: center;
      gap: 1rem;
      color: $color-primary;
      ul {
        display: flex;
        gap: 1rem;
      }
    }
  }
}
</style>
