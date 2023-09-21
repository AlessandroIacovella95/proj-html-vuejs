<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";
export default {
  data() {
    return {};
  },
  components: { AppHeader, AppMain, AppFooter },
};
</script>

<template>
  <AppHeader />
  <AppMain />
  <footer>
    <AppFooter />
  </footer>
</template>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Merriweather&family=Montserrat:wght@400;700&display=swap");
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: "Merriweather", serif;
}
footer {
  background-color: #222222;
}
</style>
