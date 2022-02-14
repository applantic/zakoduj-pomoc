<template>
  <div class="layout">
    <TheHeader />
    <div class="container">
      <Nuxt />
    </div>
    <TheFooter />
  </div>
</template>

<style scoped lang="scss">
.layout {
  font-family: Poppins, -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI",
    Roboto, "Helvetica Neue", Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.5;
  background-color: white;
  @media (min-width: $medium) {
    background-image: url(/bg-white-wave.svg),
      radial-gradient(
        circle,
        rgba(255, 255, 255, 1) 12%,
        rgba(255, 255, 255, 1) 72%
      ),
      linear-gradient(90deg, #a67fe230 0%, #ddcc8c26 100%);
    background-size: 101%, 100%, cover;
    background-repeat: no-repeat, no-repeat, repeat;
    background-position: top right, 0 54.7vw, bottom;
  }
  @media (min-width: $big) {
    background-size: 171%, 100%, cover;
    background-position: -200px -750px, 0 54.7vw, bottom;
  }
}

.layout {
  margin: 0 auto;
}

.container {
  max-width: $medium;
  margin: 0 20px;
  min-height: calc(100vh - (88px + 45px + 60px + 21px));
  @media (min-width: $small) {
    min-height: calc(100vh - (80px + 91px));
  }
  @media (min-width: $medium) {
    min-height: calc(100vh - (80px + 106px));
    margin: 0 auto;
  }
}
</style>
