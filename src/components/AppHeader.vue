<script>
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
    };
  },
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
      <font-awesome-icon class="me-4" icon="fa-solid fa-magnifying-glass" />
      <font-awesome-icon class="me-4" icon="fa-solid fa-bag-shopping" />
      <font-awesome-icon class="me-4" icon="fa-solid fa-bars" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container-fluid {
  height: 90vh;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  background-image: url("/img/h5-slide-3-background.jpg");
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
    color: white;
    font-size: 1.25rem;
    margin-top: 24px;
  }
}

.active_border {
  border-bottom: 4px solid #0c7cec;
}
</style>
