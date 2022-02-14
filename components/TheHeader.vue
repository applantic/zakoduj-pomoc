<template>
  <header class="header">
    <div class="header__container">
      <strong class="header__logo">
        <NuxtLink class="logo" to="/">Zakoduj Pomoc ❤️</NuxtLink>
      </strong>
      <nav class="nav">
        <NuxtLink class="nav__link" to="/projects/">Projekty</NuxtLink>
        <NuxtLink class="nav__link" to="/team/">Zespół</NuxtLink>
        <NuxtLink class="nav__link" to="/documents/">Dokumenty</NuxtLink>
        <NuxtLink class="nav__link" to="/contact/">Kontakt</NuxtLink>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss">
a.nuxt-link-exact-active {
  font-weight: bold;
}
.header {
  margin-bottom: 20px;
  background-color: #fff;
  filter: drop-shadow(0px -7px 10px #aaaaaa);
  font-weight: 400px;
  &__container {
    height: auto;
    display: flex;
    align-items: center;
    justify-content: center;
    max-width: $medium;
    margin: 0 auto;
    flex-wrap: wrap;
    align-content: stretch;
    @media (min-width: $small) {
      justify-content: space-between;
    }
    @media (min-width: $medium) {
      justify-content: space-between;
      height: 60px;
    }
  }
  &__logo {
    margin: 10px;
  }
}
.logo {
  color: rgb(61 58 128);
  text-decoration: none;
  margin-top: 10px;
  @media (min-width: $medium) {
    margin-top: 0;
  }
}

.nav {
  margin: 10px auto;
  @media (min-width: $small) {
    margin: 10px;
  }
  @media (min-width: $medium) {
    margin: 0;
  }

  &__link {
    text-decoration: none;
    color: rgb(61 58 128);
    margin: 5px 10px 5px 10px;
    @media (min-width: $medium) {
      margin: 0 0 0 30px;
    }
  }
}

.nav__link:hover {
  text-decoration: underline;
}
</style>
