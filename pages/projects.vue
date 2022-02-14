<template>
  <div>
    <nuxt-content :document="projectpage" />
    <section
      class="project"
      v-for="project of projects"
      :key="project.title"
      :class="{ contentactiveproject: project.active }"
    >
      <h2>{{ project.title }}</h2>
      <div class="project__container">
        <div>
          <img
            :src="project.image"
            class="project__img"
            :class="{ 'project__img-active': project.active }"
            :alt="project.title"
          />
        </div>

        <div v-if="project.active" class="project-active">
          <div class="project-active__container">
            <p class="project-active__p">Ciągle rozwijamy ten projekt,</p>
            <NuxtLink to="/contact/"> chcesz pomóc?</NuxtLink><span> 🤗</span>
          </div>
        </div>
        <nuxt-content :document="project" />
      </div>
    </section>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const projects = await $content("projects").fetch();
    const projectpage = await $content("projectpage").fetch();

    projects.sort(function (a, b) {
      return a.active > b.active ? -1 : 1;
    });
    return { projects, projectpage };
  },
};
</script>

<style scoped lang="scss">
h2 {
  margin: 15px 25px 15px 25px;
  @media (min-width: $medium) {
    margin: 35px 0 0 0;
  }
}
.contentactiveproject {
  margin-bottom: 85px;
}
.project__container::v-deep p {
  margin: 0 0 16px 0;
}

.project__container::v-deep .nuxt-content {
  @media (min-width: $medium) {
    margin: 0 0 16px 32px;
  }
}
.project {
  &__img {
    display: block;
    width: 100vw;
    max-width: 100%;
    height: fit-content;
    filter: drop-shadow(-2px 3px 6px #aaaaaa);
    border-radius: 3px;
    @media (min-width: $medium) {
      max-width: 550px;
    }
  }
  &__img-active {
    border-radius: 3px 3px 0 0;
  }
  &__container {
    display: flex;
    position: relative;
    flex-direction: column;

    @media (min-width: $medium) {
      flex-direction: row;
    }
  }
}

.project-active {
  width: 100%;
  height: 36px;
  background: linear-gradient(
    90deg,
    rgb(147 213 126) 33%,
    rgb(186 226 123) 72%
  );
  bottom: -36px;
  z-index: 1;
  font-size: 14px;
  font-weight: 700;
  /* filter: drop-shadow(-2px 3px 6px #aaaaaa); */
  box-shadow: -2px 5px 9px #cecece;
  color: black;
  border-radius: 0 0 3px 3px;
  @media (min-width: $medium) {
    width: 50%;
    position: absolute;
    bottom: -36px;
    z-index: 1;
  }
  &__container {
    text-align: center;
    padding-top: 7px;
  }
  &__p {
    display: inline;
  }
  &__a {
    font-weight: 700;
    color: black;
  }
}
</style>
