<script>
import AppMiniCard from "../Main/AppMiniCard.vue";
export default {
  data() {
    return {
      miniCards: [
        {
          image: "/img/h5-custom-icon-1.png",
          text: "Languages",
        },
        {
          image: "/img/h5-custom-icon-2.png",
          text: "Software",
        },
        {
          image: "/img/h5-custom-icon-3.png",
          text: "Business",
        },
        {
          image: "/img/h5-custom-icon-4.png",
          text: "Chemistry",
        },
        {
          image: "/img/h5-custom-icon-5.png",
          text: "Science",
        },
        {
          image: "/img/h5-custom-icon-6.png",
          text: "DIY&Craft",
        },
      ],
    };
  },
  components: { AppMiniCard },
};
</script>

<template>
  <section>
    <div class="container d-flex gap-5 justify-content-between">
      <AppMiniCard
        v-for="miniCard in miniCards"
        :image="miniCard.image"
        :text="miniCard.text"
      />
    </div>
  </section>
</template>

<style lang="scss" scoped></style>
