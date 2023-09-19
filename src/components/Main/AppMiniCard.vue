<script>
export default {
  data() {
    return {};
  },
  props: {
    image: String,
    text: String,
  },
};
</script>

<template>
  <div class="card mt-4">
    <img :src="image" alt="" />
    <h5 class="mt-4">{{ text }}</h5>
  </div>
</template>

<style lang="scss" scoped>
.card {
  height: 180px;
  width: 250px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #f2f8fc;
  img {
    width: 80px;
    max-width: 100%;
  }

  h5 {
    font-size: 1rem;
    font-weight: bold;
  }
}
</style>
