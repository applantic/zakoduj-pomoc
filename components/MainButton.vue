<template>
  <NuxtLink class="wrapper" :to="{ path: link }">
    <div class="button">
      {{ message }}
    </div>
  </NuxtLink>
</template>

<script>
export default {
  name: "MainButton",
  props: {
    link: String,
  },
  data() {
    return {
      message: "Dowiedz się więcej",
    };
  },
};
</script>

<style lang="scss">
.wrapper {
  width: fit-content;
  color: #fff;
  text-decoration: none;
  background-color: rgb(174 176 255);
  border-radius: 8px;
  margin-bottom: 10px;
}
.button {
  font-size: 14px;
  border: none;
  font-weight: 500;
  box-shadow: rgb(0 0 0 / 8%) 0px 1px 3px;
  padding: 10px 28px;
  @media (min-width: $medium) {
    box-shadow: rgb(0 0 0 / 25%) 0px 3px 5px;
    padding: 12px 32px;
    font-size: 16px;
    border-radius: 8px;
  }
}
.cta {
  background-color: #e1cc90;
}

.cta a {
  color: #464b97;
}
</style>
