<script>
export default {
  data() {
    return {};
  },
  props: {
    text: String,
    current: Boolean,
  },
};
</script>

<template>
  <li>{{ text }}</li>
</template>

<style lang="scss" scoped></style>
