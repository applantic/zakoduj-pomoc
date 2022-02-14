<template>
  <footer>
    <p>Fundacja Zakoduj Pomoc 2022.</p>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style>
footer {
  margin: 0;
  margin-top: 60px;
  text-align: center;
  display: flex;
  justify-content: center;
  /* margin-right: calc((100vw - (1200px/2))*1); */
  /* margin-left: -121px; */
  background: linear-gradient(90deg, #ddcc8c26 0%, #a67fe230 100%);
  /* background-color: #fff; */
  filter: drop-shadow(0px 11px 10px #aaaaaa);
  min-height: 30px;
  max-height: 45px;
}
footer p {
  font-size: 13px;
  color: black;
}
</style>
