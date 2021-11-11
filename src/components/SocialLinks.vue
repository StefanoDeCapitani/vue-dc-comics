<template>
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
</template>

<script>
export default {
  name: "SocialLinks",
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
.social {
  margin-left: auto;
  display: flex;
  align-items: center;
  gap: 2rem;
  color: $color-primary;
  ul {
    display: flex;
    gap: 1rem;
  }
}
</style>
