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
    <div class="button_custom"><a href="#start">Go Top</a></div>
  </header>
</template>

<style lang="scss" scoped>
// header {
//   background-image: url("/img/h5-slide-3-background.jpg");
// }
.button_custom {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 65px;
  aspect-ratio: 1;
  position: fixed;
  bottom: 20px;
  right: 15px;
  z-index: 99;
  border: none;
  outline: none;
  background-color: #40c4ff;
  padding: 15px;
  font-size: 15px;
  cursor: pointer;
  a {
    text-decoration: none;
    color: white;
    font-size: 0.8rem;
    white-space: nowrap;
  }
}
</style>
