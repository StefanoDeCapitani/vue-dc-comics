<template>
  <header class="header">
    <div class="container">
      <a href="#">
        <img src="../assets/img/dc-logo.png" alt="Logo DC comics" />
      </a>
      <nav class="nav">
        <ul class="nav__ul">
          <li class="nav__list-item">
            <a class="nav__link" href="#">Link</a>
          </li>
          <li class="nav__list-item">
            <a class="nav__link" href="#">Link</a>
          </li>
          <li class="nav__list-item">
            <a class="nav__link" href="#">Link</a>
          </li>
          <li class="nav__list-item">
            <a class="nav__link" href="#">Link</a>
          </li>
          <li class="nav__list-item">
            <a class="nav__link" href="#">Link</a>
          </li>
          <li class="nav__list-item">
            <a class="nav__link" href="#">Link</a>
          </li>
          <li class="nav__list-item">
            <a class="nav__link" href="#">Link</a>
          </li>
          <li class="nav__list-item">
            <a class="nav__link" href="#">Link</a>
          </li>
          <li class="nav__list-item">
            <a class="nav__link" href="#">Link</a>
          </li>
          <li class="nav__list-item">
            <a class="nav__link" href="#">Link</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped lang="scss">
.container {
  max-width: 1280px;
  display: flex;
  .nav {
    margin-left: auto;
  }
}
</style>
