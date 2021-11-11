<template>
  <nav class="site-map">
    <div class="container site-map__container">
      <div
        class="site-map__category"
        v-for="(category, i) in siteMapLinks"
        :key="i"
      >
        <h3 class="site-map__tag">{{ category.tag }}</h3>
        <ul class="site-map__ul">
          <li
            class="site-map__li"
            v-for="(link, i) in category.linksList"
            :key="i"
          >
            <a class="site-map__link" :href="link.href">
              {{ link.text }}
            </a>
          </li>
        </ul>
      </div>
      <img class="logo-bg" src="../assets/img/dc-logo-bg.png" alt="Logo DC" />
    </div>
  </nav>
</template>

<script>
export default {
  name: "SiteMap",
  data() {
    return {
      siteMapLinks: [
        {
          tag: "DC COMICS",

          linksList: [
            { text: "Characters", href: "#" },
            { text: "Comics", href: "#" },
            { text: "Movies", href: "#" },
            { text: "Tv", href: "#" },
            { text: "Games", href: "#" },
            { text: "Videos", href: "#" },
            { text: "News", href: "#" },
          ],
        },
        {
          tag: "SHOP",

          linksList: [
            { text: "Shop DC", href: "#" },
            { text: "Shop DC Collectibles", href: "#" },
          ],
        },

        {
          tag: "DC",

          linksList: [
            { text: "Term Of Use", href: "#" },
            { text: "Privacy Policy (New)", href: "#" },
            { text: "Ad Choices", href: "#" },
            { text: "Advertising", href: "#" },
            { text: "Jobs", href: "#" },
            { text: "Subscriptions", href: "#" },
            { text: "Talent Workshops", href: "#" },
            { text: "CPSC Certificates", href: "#" },
            { text: "Ratings", href: "#" },
            { text: "Shop Help", href: "#" },
            { text: "Contact Us", href: "#" },
          ],
        },

        {
          tag: "SITES",

          linksList: [
            { text: "DC", href: "#" },
            { text: "MAD Magazine", href: "#" },
            { text: "DC Kids", href: "#" },
            { text: "DC Universe", href: "#" },
            { text: "DC Power Visa", href: "#" },
          ],
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/styles/variables";
.site-map {
  position: relative;
  background-image: url("../assets/img/footer-bg.jpg");
  background-size: cover;
  background-position: center;
  padding: $padding-40 0;
  overflow: hidden;

  .site-map__container {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    align-content: flex-start;
    gap: 1rem 2rem;
    height: 300px;

    .site-map__category {
      display: flex;
      flex: 0 0 auto;
      flex-direction: column;
      gap: 1rem;

      .site-map__tag {
        color: white;
      }
      .site-map__ul {
        display: flex;
        flex-direction: column;
        gap: 0.3rem;
        .site-map__link {
          color: rgba(255, 255, 255, 0.233);
        }
      }
    }

    .logo-bg {
      position: absolute;
      top: 50%;
      left: 70%;
      transform: translate(-50%, -50%);
    }
  }
}
</style>
