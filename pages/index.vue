<template>
  <div class="index">
    <section class="main-section">
      <div class="content">
        <h1>Budujemy software dla&nbsp;fundacji charytatywnych</h1>
        <p class="hero__p">
          Nasi wolontariusze pracują ciężko, <br />
          żebyście Wy mogli pracować lżej
        </p>
      </div>
      <img alt="Example image" src="/laptop.png" class="image image--main" />
    </section>
    <section>
      <img alt="Example image" src="/calender.png" class="image image--left" />
      <div class="content">
        <h2>Potrzebujesz Pomocy?</h2>
        <p>
          Skontaktuj sie z nami. Opisz nam swój problem i jeśli będziemy w
          stanie pomóc, umówimy się na spotkanie.
        </p>
        <MainButton link="contact" />
      </div>
    </section>
    <section>
      <div class="content">
        <h2>Zobacz nasze projekty.</h2>
        <p>
          Do każdego projektu podchodzimy indywidualnie. Skupiamy się na
          rozwiazywaniu problemów i przejrzystym designie.
        </p>
        <MainButton link="projects" />
      </div>
      <img alt="Example image" class="image" src="/folder.png" />
    </section>
  </div>
</template>

<script>
export default {
  layout: "home",
  name: "IndexPage",
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
</style>

<style scoped lang="scss">
h1 {
  font-weight: bold;
  font-size: 2em;
  line-height: 34px;
  margin: 0.5rem 0;
  @media (min-width: $medium) {
    font-size: 3.125em;
    line-height: 1.275em;
  }
}

h2 {
  color: #3d3a80;
  font-size: 1.5em;
  margin: 0.1rem 0;
  @media (min-width: $medium) {
    font-size: 2.5em;
    margin: 0.2rem 0;
  }
}

p {
  color: #5d6b99;
  font-size: 1em;
  font-weight: 500;
  margin: 5px 0 15px 0;
  @media (min-width: $medium) {
    font-size: 1.375em;
    line-height: 1.375em;
    margin: 5px;
  }
}
.main-section {
  color: #3d3a80;
  align-items: flex-start;
  @media (min-width: $medium) {
    padding-top: 50px;
  }
}

.main-section .project {
  padding-top: 30px;
}

section {
  display: flex;
  position: relative;
  @media (min-width: $medium) {
    height: auto;
  }
}

.hero__p {
  margin-top: 15px;
}

.content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  z-index: 2;
  margin-bottom: 10px;
}

.home-links a {
  margin-right: 1rem;
}

.image {
  max-width: 50px;
  margin: 15px 30px;
  position: absolute;
  z-index: 1;
  top: 1px;
  left: 1px;
  display: none;
  @media (min-width: $medium) {
    z-index: auto;
    display: inline;
    position: static;
    max-width: 430px;
  }
  &--main {
    max-width: 110px;
    @media (min-width: $medium) {
      max-width: 500px;
    }
  }
  &--left {
    padding-right: 20px;
  }
}
</style>
