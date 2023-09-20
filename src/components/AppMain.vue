<script>
import AppMiniCards from "./Main/AppMiniCards.vue";
import AppCards from "./Main/AppCards.vue";
import List from "./Main/List.vue";
import AppTable from "./Main/AppTable.vue";
export default {
  data() {
    return {
      list_items: [
        {
          text: "What We Do",
          current: true,
        },
        {
          text: "Degree Programme",
          current: false,
        },
        {
          text: "Career Achievements",
          current: false,
        },
        {
          text: "Personal Managment",
          current: false,
        },
        {
          text: "Steps To Success",
          current: false,
        },
        {
          text: "Knowledge Transfer",
          current: false,
        },
      ],
      list_objects: [
        {
          text: "We enrich lives through learning",
          current: true,
        },
        {
          text: "Maximizing potential through individual attention",
          current: false,
        },
        {
          text: "The trusted name for specialized training",
          current: false,
        },
        {
          text: "People teach. People learn. This is where they connect",
          current: false,
        },
      ],
    };
  },
  methods: {
    toggleCurrent(index) {
      this.list_items.forEach((item, i) => {
        item.current = i == index;
      });
    },
  },

  components: { AppMiniCards, List, AppCards, AppTable },
};
</script>

<template>
  <AppMiniCards />
  <section class="container">
    <div class="row">
      <div class="col d-flex flex-column align-items-start">
        <h2>The Trusted Name <br />for In-Home Tutoring</h2>
        <p class="mt-4">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Dignissimos,
          ipsa magnam sequi itaque modi illo facere veniam, corporis facilis a,
          velit nihil excepturi. Accusantium harum libero omnis consectetur,
          amet corrupti.
        </p>
        <a href="#">LEARN MORE</a>
        <div class="img_container">
          <img src="/img/h5-img-1.jpg" alt="" />
        </div>
      </div>
    </div>
  </section>
  <section class="container mt-5">
    <div class="row">
      <div class="col d-flex justify-content-center">
        <div>
          <img class="custom_img" src="/img/h9-slide-img-2.png" alt="" />
        </div>
        <div>
          <h2>
            Empowering <br />
            Childern to Reach <br />Their Potential
          </h2>
          <p class="mt-4">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aut nihil
            amet a est, excepturi optio deleniti soluta cum expedita. Est in
            earum illo animi ipsa nobis non magnam officia doloribus?Lorem ipsum
            dolor sit amet consectetur, adipisicing elit. Rem ipsam pariatur
            minima cum fugiat quidem sit ea animi iste recusandae voluptatum
            tempore dolorum libero culpa, maiores quam corporis cumque iusto?
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
      </div>
    </div>
  </section>
  <section class="bg_img d-flex justify-content-center align-items-center">
    <div class="container text-center">
      <div class="row">
        <div class="col text-light">
          <img
            class="mb-3"
            src="/img/testimonials-standard-2.png"
            alt="testimonials"
          />
          <p class="mb-4 text-light">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ad veniam
            ratione atque labore. Iusto sapiente ex magnam. Eos voluptatum
            labore velit temporibus, doloribus facilis voluptas iure ut at
            maiores iusto?
          </p>
          <h6>Joan Collins</h6>
          <span>Student</span>
          <div
            class="d-flex justify-content-center align-items-center text-light"
          >
            <div class="circle"></div>
            <div class="circle slide_active"></div>
            <div class="circle"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="container">
    <div class="row">
      <div class="col-3">
        <ul class="list_items">
          <List
            v-for="(item, index) in list_items"
            :text="item.text"
            :class="{ items: item, active_border: item.current }"
            @click="toggleCurrent(index)"
          />
        </ul>
      </div>
      <div class="col-7">
        <h3>Learning Possibilities</h3>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nihil minima
          laudantium quis laboriosam repellat quod iure quas voluptatem ratione
          ad fuga, odit ea est saepe optio id rerum eaque neque. Lorem ipsum
          dolor sit amet, consectetur adipisicing elit. Dolor aut ad, odio
          itaque repudiandae eligendi eos commodi, repellendus eum atque dolore
          ipsa. Expedita sed voluptate eum at quod minus ipsum?
        </p>
        <ul class="list_items">
          <List v-for="object in list_objects" :text="object.text" />
        </ul>
        <img class="logo" src="/img/h12-tabs-icon-1.png" alt="" />
      </div>
    </div>
  </section>
  <section class="bg_section container text-center">
    <div class="text_content">
      <h2>Popular Online Courses</h2>
      <p>
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptatem ab
        eligendi delectus voluptatibus, dignissimos officia pariatur dolore
        adipisci labore obcaecati quidem veniam maiores iure itaque perspiciatis
        consectetur omnis reiciendis tenetur?
      </p>
    </div>
    <AppCards />
    <div class="d-flex justify-content-center">
      <div class="circle"></div>
      <div class="circle slide_active"></div>
      <div class="circle"></div>
    </div>
  </section>
  <section class="bg_section text-center">
    <div class="container">
      <h2>Pricing Plans</h2>
      <p>
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ducimus atque
        illum autem distinctio quos asperiores voluptatibus rerum tenetur minus.
      </p>
    </div>

    <div class="container d-flex justify-content-center">
      <div class="logo_table">
        <img src="/img/logo-table.png" alt="logo_table" />
      </div>
      <div class="logo_cart d-flex justify-content-center align-items-center">
        <font-awesome-icon icon="fa-solid fa-cart-shopping" />
      </div>
      <AppTable />
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
  .circle {
    margin-top: 100px;
    margin-right: 5px;
    margin-left: 5px;
    width: 14px;
    aspect-ratio: 1;
    background-color: #ffffff80;
    border-radius: 50%;
    cursor: pointer;
  }

  .slide_active {
    background-color: white;
  }
}

.list_items {
  list-style: none;
  padding-left: 0;

  .active_border {
    border-left: 4px solid #40c4ff !important;
    color: #40c4ff !important;
  }
  .items {
    color: #898989;
    font-weight: 600;
    font-size: 1.1rem;
    border: 1px solid #e5e5e5;
    width: 250px;
    padding: 20px;
    white-space: nowrap;
    cursor: pointer;
  }
}

.col-7 {
  position: relative;
  .logo {
    position: absolute;
    bottom: 15px;
    right: 0;
    width: 110px;
  }
}

.col-7 {
  h3 {
    font-size: 2.5rem;
    margin-bottom: 20px;
  }
  p {
    font-size: 1.1rem;
  }

  li {
    margin-top: 14px;
    color: #ababab;
    font-size: 1.1rem;
  }

  li::before {
    content: "✓";
    color: #40c4ff;
    margin-right: 10px;
  }
}
.bg_section {
  background-image: url("/img/page-background-img.png");
  .text_content {
    p {
      padding: 0 100px;
      color: #959595;
      font-size: 1.1rem;
      margin-top: 25px;
    }
  }
  .circle {
    margin-top: 100px;
    margin-right: 5px;
    margin-left: 5px;
    width: 14px;
    aspect-ratio: 1;
    background-color: #9ce0ff;
    border-radius: 50%;
    cursor: pointer;
  }

  .slide_active {
    background-color: #40c4ff;
  }
  .container {
    position: relative;
    .logo_table {
      border: 1px solid #959595;
      border-left: 0;
      position: absolute;
      top: 30px;
      right: 190px;
      cursor: pointer;
    }

    .logo_cart {
      color: #ee2852;
      width: 56px;
      aspect-ratio: 1;
      font-size: 1.5rem;
      border: 1px solid #959595;
      border-left: 0;
      position: absolute;
      top: 100px;
      right: 190px;
      cursor: pointer;
    }
  }
}
</style>
