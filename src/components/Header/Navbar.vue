<script>
import ButtonApp from "../AppButton.vue";
export default {
  data() {
    return {
      links: [
        {
          text: "HOME",
          url: "#",
          current: true,
        },
        {
          text: "COURSES",
          url: "#",
          current: false,
        },
        {
          text: "INSTRUCTORS",
          url: "#",
          current: false,
        },
        {
          text: "EVENTS",
          url: "#",
          current: false,
        },
        {
          text: "PAGES",
          url: "#",
          current: false,
        },
        {
          text: "ELEMENTS",
          url: "#",
          current: false,
        },
      ],
      buttonPrimary: "button_primary",
      buttonText: "REGISTER NOW",
    };
  },

  components: { ButtonApp },
  methods: {
    toggleCurrent(index) {
      this.links.forEach((link, i) => {
        link.current = i == index;
      });
    },
  },
};
</script>

<template>
  <div class="container-fluid">
    <div class="navbar">
      <img class="logo mt-4 ms-4" src="/img/logo-light.png" alt="logo" />
      <ul>
        <li
          v-for="(link, index) in links"
          :class="{ active_border: link.current }"
        >
          <a
            :href="link.url"
            @click="toggleCurrent(index)"
            :class="{ active: link.current }"
          >
            {{ link.text }}
          </a>
        </li>
      </ul>
      <div class="icons">
        <span> 0 </span>
        <font-awesome-icon class="me-4" icon="fa-solid fa-magnifying-glass" />
        <font-awesome-icon class="me-4" icon="fa-solid fa-bag-shopping" />
        <font-awesome-icon class="me-4" icon="fa-solid fa-bars" />
      </div>
    </div>
    <div class="text-center header_text">
      <h1 class="text-light">Contemporary Ideas</h1>
      <p class="text-light">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem, vitae
        suscipit. Velit dolores veritatis similique.
      </p>
      <ButtonApp :customButton="buttonPrimary" :text="buttonText" />
    </div>
    <div class="d-flex justify-content-center align-items-center text-light">
      <div class="circle"></div>
      <div class="circle"></div>
      <div class="circle"><div class="slide_point"></div></div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container-fluid {
  height: 90vh;
  .navbar {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
  }
  .logo {
    width: 200px;
    cursor: pointer;
  }

  ul {
    display: flex;
    align-items: center;
    list-style: none;
    gap: 1.2rem;
    font-size: 0.95rem;
    font-weight: 700;
    margin-top: 32px;

    li {
      margin-right: 30px;
    }
  }

  a {
    text-decoration: none;
    color: white;
    .active {
      color: #0c7cec;
    }
  }

  .icons {
    position: relative;
    color: white;
    font-size: 1.2rem;
    margin-top: 27px;
    span {
      position: absolute;
      top: 2px;
      left: 55px;
      font-size: 0.8rem;
      width: 15px;
      background-color: #40c4ff;
      line-height: 15px;
      padding-left: 4px;

      aspect-ratio: 1;
      border-radius: 50%;
    }

    .fa-magnifying-glass,
    .fa-bag-shopping,
    .fa-bars {
      cursor: pointer;
    }
  }
}

.header_text {
  height: 80%;
  width: 650px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  h1 {
    font-size: 3rem;
    font-weight: 700;
  }
  p {
    font-size: 1.5rem;
  }
  .button_primary {
    width: 250px;
    height: 70px;
    border: #40c4ff;
    margin: 20px auto;
    border-radius: 0;
    color: white;
    background-color: #40c4ff;
    font-weight: 700;
    cursor: pointer;
  }
}
.circle {
  margin-right: 10px;
  width: 25px;
  aspect-ratio: 1;
  background-color: #00000066;
  border-radius: 50%;
  cursor: pointer;
}

.circle:last-child {
  border: 2px solid white;
  background-color: transparent;
  display: flex;
  align-items: center;
  justify-content: center;
  .slide_point {
    width: 6px;
    aspect-ratio: 1;
    background-color: white;
    border-radius: 50%;
  }
}

.active_border {
  border-bottom: 4px solid #0c7cec;
}
</style>
