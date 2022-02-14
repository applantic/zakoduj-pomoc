<template>
  <div>
    <nuxt-content :document="documents" />
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const documents = await $content("documents").fetch();

    return { documents };
  },
};
</script>
