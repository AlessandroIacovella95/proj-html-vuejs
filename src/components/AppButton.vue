<script>
export default {
  data() {
    return {};
  },
  props: { customButton: String, text: String },
};
</script>

<template>
  <button type="button" :class="customButton">{{ text }}</button>
</template>

<style lang="scss" scoped></style>
