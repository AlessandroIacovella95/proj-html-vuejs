<script>
export default {
  data() {
    return {};
  },
  props: {
    img: String,
    url: String,
  },
};
</script>

<template>
  <img :src="img" alt="" />
</template>

<style lang="scss" scoped></style>
