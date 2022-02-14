<template>
  <div class="layout">
    <TheHeader />
    <div class="container">
      <transition name="layout">
        <Nuxt />
      </transition>
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
  background-color: #fff;
  margin: 0 auto;
  color: #3d3a80;
}
p {
  color: #1d1c3d;
}

.container::v-deep .nuxt-content p,
.container::v-deep .nuxt-content h1,
.container::v-deep .nuxt-content h2 {
  margin: 15px 25px 15px 25px;
  @media (min-width: $small) {
    margin-left: 15px;
    margin-right: 15px;
  }
  @media (min-width: $medium) {
    margin-left: 0;
    margin-right: 0;
  }
}

h1 {
  color: red;
}

.container {
  max-width: $medium;
  min-height: calc(100vh - (88px + 126px));
  margin: 0 auto;
  @media (min-width: $small) {
    min-height: calc(100vh - (80px + 91px));
  }
  @media (min-width: $medium) {
    min-height: calc(100vh - (80px + 106px));
  }
}
</style>
