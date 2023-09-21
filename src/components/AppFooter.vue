<script>
import List from "./Main/List.vue";
import FooterList from "./Footer/FooterList.vue";
export default {
  data() {
    return {
      list_Academy: [
        {
          text: "Providing Life Changing",
          url: "#",
          current: false,
        },
        {
          text: "Experiences Through",
          url: "#",
          current: false,
        },
        {
          text: "Education. Class That Fit Your",
          url: "#",
          current: false,
        },
        {
          text: "BUsy Life. Closer to Home",
          url: "#",
          current: false,
        },
      ],
      courses: [
        {
          title: "Business English",
          text: "Preston Marshall",
          url: "#",
          current: false,
        },
        {
          title: "Social Computing",
          text: "David Sanders",
          url: "#",
          current: false,
        },
        {
          title: "Learn Spanish",
          text: "Jennie King",
          url: "#",
          current: false,
        },
      ],
      supports: [
        {
          text: "User dashboard",
          current: false,
        },
        {
          text: "Contact Us",
          current: false,
        },
        {
          text: "FAQ",
          current: false,
        },
        {
          text: "Course Offer",
          current: false,
        },
        {
          text: "Events",
          current: false,
        },
      ],
    };
  },
  components: { List, FooterList },
  methods: {
    toggleActive(item, index, myArray) {
      myArray.forEach((item, i) => {
        item.current = i == index;
      });
    },
  },
};
</script>

<template>
  <div class="container d-flex justify-content-between">
    <div class="me-5">
      <img class="logo_footer" src="/img/footer-logo-1.png" alt="logo-footer" />
      <ul class="list_items">
        <List
          v-for="(element, index) in list_Academy"
          :text="element.text"
          :class="{ items: element, active: element.current }"
          @click="toggleActive(element, index, list_Academy)"
        />
      </ul>
      <p class="text-light mt-5">
        <font-awesome-icon icon="fa-solid fa-phone" /> 1-677-124-44227
      </p>
      <p class="text-light">
        <font-awesome-icon icon="fa-regular fa-clock" /> Mon - Sat 8.00 - 18.00
      </p>
    </div>
    <div class="container_list">
      <h3 class="text-light">Popular Courses</h3>
      <ul class="list_items">
        <FooterList
          v-for="(course, index) in courses"
          :title="course.title"
          :text="course.text"
          :class="{ items: course, active: course.current }"
          @click="toggleActive(course, index, courses)"
        />
      </ul>
    </div>
    <div>
      <h3 class="text-light title">Support</h3>
      <ul class="list_items">
        <List
          v-for="(support, index) in supports"
          :text="support.text"
          :class="{ items: support, active: support.current }"
          @click="toggleActive(support, index, supports)"
        />
      </ul>
    </div>
    <div>
      <h3 class="text-light title">Flexible Learning</h3>
      <img class="world_img" src="/img/footer-img-1.png" alt="img_world" />
    </div>
  </div>
  <section>
    <div class="container d-flex">
      <div class="container footer_bottom">
        <p class="mt-5">Copyrights 2017 Mikado Themes</p>
      </div>
      <div class="d-flex info">
        <p class="mt-5">CALL +44 300 303 0266</p>
        <p class="mt-5">FOLLOW US</p>
        <span class="mt-5"
          ><font-awesome-icon icon="fa-brands fa-twitter"
        /></span>
        <span class="mt-5"
          ><font-awesome-icon icon="fa-brands fa-square-instagram"
        /></span>
        <span class="mt-5"
          ><font-awesome-icon icon="fa-brands fa-facebook"
        /></span>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.container {
  margin-top: 50px;
  padding-top: 150px;
  .list_items {
    list-style: none;
    padding-left: 0;
    margin-bottom: 0;

    .items {
      color: #898989;
      font-weight: 600;
      font-size: 1rem;
      width: 250px;
      padding: 5px 0;
      cursor: pointer;
    }

    .active {
      color: white;
    }
  }

  .logo_footer {
    width: 180px;
    margin-bottom: 30px;
  }

  .container_list {
    h3 {
      margin-bottom: 30px;
    }
    h5 {
      margin-bottom: 0;
    }
    li {
      margin-bottom: 15px;
    }
  }

  .title {
    margin-bottom: 30px;
  }
  .world_img {
    width: 250px;
  }
}

section {
  .container {
    border-top: 1px solid #898989;
    padding-top: 0;
    .footer_bottom {
      margin: 0 auto;
    }
    p {
      font-size: 0.9rem;
      margin-bottom: 0;
      color: #898989;
    }
  }
  .info {
    color: #898989;
    margin-bottom: 30px;
    p {
      white-space: nowrap;
      font-size: 0.9rem;
      margin-right: 15px;
    }

    span {
      margin-right: 15px;
    }
  }
}
</style>
