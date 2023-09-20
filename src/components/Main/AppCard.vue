<script>
export default {
  data() {
    return {};
  },
  props: {
    text: String,
    icon: String,
    image: String,
    title: String,
    badge: String,
    badgeColor: String,
    author: String,
    description: String,
  },
  computed: {
    badgeClass() {
      return {
        badge: true,
        "badge-yellow": this.badgeColor === "yellow",
        "badge-blue": this.badgeColor === "blue",
      };
    },
  },
};
</script>

<template>
  <div class="card">
    <img :src="image" class="card-img-top" alt="" />
    <div class="card-body text-start">
      <h6>{{ title }}</h6>
      <span class="author">{{ author }}</span>
      <span :class="badgeClass">{{ badge }}</span>
      <p class="card_text">{{ description }}</p>
      <div class="icon">
        <span> <font-awesome-icon icon="fa-solid fa-user" /> 1 </span>
        <span><font-awesome-icon icon="fa-solid fa-tag" /></span>
        <span class="text">{{ text }}</span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  width: 300px;
  .card-body {
    position: relative;

    .author {
      color: #b9b9b9;
    }

    .badge {
      width: 40px;
      height: 20px;
      position: absolute;
      top: 18px;
      right: 20px;
    }
    .badge-yellow {
      background-color: #ffd740;
    }
    .badge-blue {
      background-color: #40c4ff;
    }

    .card_text {
      margin-top: 20px;
    }

    .icon {
      color: #898989;
      .fa-user {
        margin-right: 10px;
        font-size: 15px;
      }
      .fa-tag {
        margin-left: 10px;
        font-size: 15px;
      }

      .text {
        font-size: 0.8rem;
        font-weight: 600;
        margin-left: 10px;
      }
    }
  }
}
</style>
