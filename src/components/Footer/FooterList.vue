<script>
export default {
  data() {
    return {};
  },
  props: {
    title: String,
    text: String,
    current: Boolean,
  },
};
</script>

<template>
  <li>
    <h5>{{ title }}</h5>
    <span>{{ text }}</span>
  </li>
</template>

<style lang="scss" scoped></style>
