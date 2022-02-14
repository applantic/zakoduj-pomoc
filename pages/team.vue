<template>
  <div>
    <nuxt-content :document="team" />
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const team = await $content("team").fetch();

    return { team };
  },
};
</script>
