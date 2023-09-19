<script>
import AppMiniCards from "./Main/AppMiniCards.vue";
export default {
  data() {
    return {};
  },
  components: { AppMiniCards },
};
</script>

<template>
  <AppMiniCards />
  <section class="container d-flex flex-column align-items-start">
    <h2>The Trusted Name <br />for In-Home Tutoring</h2>
    <p class="mt-4">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Dignissimos, ipsa
      magnam sequi itaque modi illo facere veniam, corporis facilis a, velit
      nihil excepturi. Accusantium harum libero omnis consectetur, amet
      corrupti.
    </p>
    <a href="#">LEARN MORE</a>
    <div class="img_container">
      <img src="/img/h5-img-1.jpg" alt="" />
    </div>
  </section>
</template>

<style lang="scss" scoped>
h2 {
  font-size: 3rem;
  font-weight: 600;
  margin-top: 50px;
}
p {
  color: #ababab;
}
a {
  text-decoration: none;
  font-size: 0.9rem;
  font-weight: bold;
  color: #40c4ff;
}

.img_container {
  margin: 0 auto;
}
</style>
