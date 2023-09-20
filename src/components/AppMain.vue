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
  <section class="container d-flex justify-content-center mt-5">
    <div>
      <img class="custom_img" src="/img/h9-slide-img-2.png" alt="" />
    </div>
    <div>
      <h2>
        Empowering <br />
        Childern to Reach <br />Their Potential
      </h2>
      <p class="mt-4">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Aut nihil amet
        a est, excepturi optio deleniti soluta cum expedita. Est in earum illo
        animi ipsa nobis non magnam officia doloribus?Lorem ipsum dolor sit amet
        consectetur, adipisicing elit. Rem ipsam pariatur minima cum fugiat
        quidem sit ea animi iste recusandae voluptatum tempore dolorum libero
        culpa, maiores quam corporis cumque iusto?
      </p>
      <div class="container_user d-flex align-items-start">
        <div class="d-flex flex-column me-5">
          <span class="number">168</span>
          <span class="text">User Stories</span>
        </div>
        <div class="d-flex flex-column ms-5">
          <span class="number">347</span>
          <span class="text">Events</span>
        </div>
      </div>
    </div>
  </section>
  <section class="bg_img d-flex justify-content-center align-items-center">
    <div class="text-center text-light">
      <img
        class="mb-3"
        src="../../public/img/testimonials-standard-2.png"
        alt="testimonials"
      />
      <p class="mb-4">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ad veniam
        ratione atque labore. Iusto sapiente ex magnam. Eos voluptatum labore
        velit temporibus, doloribus facilis voluptas iure ut at maiores iusto?
      </p>
      <h6>Joan Collins</h6>
      <span>Student</span>
    </div>
  </section>
</template>

<style lang="scss" scoped>
section {
  margin-top: 70px !important;
}
.container {
  h2 {
    font-size: 3rem;
    font-weight: 600;
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
}

.custom_img {
  width: 400px;
  margin-right: 150px;
  padding-left: 50px;
}

.container_user {
  span {
    color: #40c4ff;
  }
  .number {
    font-weight: bold;
    font-size: 3.5rem;
  }
  .text {
    font-weight: 700;
    margin-left: 5px;
  }
}

.bg_img {
  height: 710px;
  background-image: url("/img/h5-parallax-img-1.png");
  background-position: top;
  div {
    width: 700px;
    p {
      font-size: 1.2rem;
    }
    h6 {
      font-size: x-large;
    }
    span {
      font-weight: 700;
    }
  }
}
</style>
