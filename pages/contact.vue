<template>
  <div>
    <nuxt-content :document="contact" />
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const contact = await $content("contact").fetch();

    return { contact };
  },
};
</script>

<style lang="scss"></style>
