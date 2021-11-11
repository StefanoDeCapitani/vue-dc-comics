<template>
  <header class="page__header">
    <div class="container">
      <a class="logo" href="#">
        <img src="../assets/img/dc-logo.png" alt="Logo DC comics" />
      </a>
      <nav class="nav">
        <ul class="nav__ul">
          <li
            v-for="(link, i) in linksList"
            :key="i"
            class="nav__li"
            :class="{ active: isCurrentLink(i) }"
          >
            <a class="nav__link" :href="link.href">
              {{ link.text }}
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {
    currentLink: Number,
  },
  data() {
    return {
      linksList: [
        { text: "characters", href: "#" },
        { text: "comics", href: "#" },
        { text: "movies", href: "#" },
        { text: "tv", href: "#" },
        { text: "games", href: "#" },
        { text: "collectibles", href: "#" },
        { text: "videos", href: "#" },
        { text: "fans", href: "#" },
        { text: "news", href: "#" },
        { text: "shop", href: "#" },
      ],
    };
  },
  methods: {
    isCurrentLink(i) {
      return i === this.currentLink;
    },
  },
};
</script>

<style scoped lang="scss">
@import "../assets/styles/variables";
.container {
  display: flex;
  align-items: center;
  .logo {
    height: 80px;
    img {
      height: 100%;
    }
  }
  .nav {
    margin-left: auto;
    .nav__ul {
      display: flex;
      gap: 0.7rem;
      .nav__li {
        position: relative;

        &::after {
          content: "";
          position: absolute;
          bottom: 0;
          left: 0rem;
          right: 100%;
          height: 5px;
          background-color: $color-primary;
        }
        &.active {
          .nav__link {
            color: $color-primary;
          }
          &::after {
            right: 0rem;
          }
        }

        .nav__link {
          padding: $padding-50 0;
          text-transform: uppercase;
          font-size: 0.7rem;
          font-weight: 500;
        }
      }
    }
  }
}
</style>
