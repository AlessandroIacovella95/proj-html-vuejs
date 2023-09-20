<script>
import Navbar from "./Header/Navbar.vue";
export default {
  data() {
    return {};
  },
  components: { Navbar },
};
</script>

<template>
  <header>
    <Navbar />
  </header>
</template>

<style lang="scss" scoped>
header {
  background-image: url("/img/h5-slide-3-background.jpg");
}
</style>
