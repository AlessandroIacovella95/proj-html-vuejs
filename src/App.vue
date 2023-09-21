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
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
footer {
  background-color: #222222;
}
</style>
