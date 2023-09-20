<script>
import AppCard from "./AppCard.vue";
export default {
  data() {
    return {
      Cards: [
        {
          text: "PROGRAMMING",
          badge: "FREE",
          badgeColor: "yellow",
          image: "/img/course-5-f-img.jpg",
          title: "Android Developer",
          author: "David Sanders",
          description:
            "Lorem ipsum dolor sit amet, te eros consulatu pro, quel labores petentium non sea, atqui posidonium interpretaris.",
        },
        {
          text: "PROGRAMMING",
          badge: "FREE",
          badgeColor: "yellow",
          image: "/img/course-6-f-img.jpg",
          title: "Web Designing",
          author: "Jennifer Powell",
          description:
            "Lorem ipsum dolor sit amet, te eros consulatu pro, quel labores petentium non sea, atqui posidonium interpretaris.",
        },
        {
          text: "BUSINESS",
          badge: "$20",
          badgeColor: "blue",
          image: "/img/course-12-f-img.jpg",
          title: "Financial Modeling",
          author: "Edward Bowman",
          description:
            "Lorem ipsum dolor sit amet, te eros consulatu pro, quel labores petentium non sea, atqui posidonium interpretaris.",
        },
      ],
    };
  },
  components: { AppCard },
};
</script>

<template>
  <div class="container">
    <div class="row">
      <div class="col d-flex justify-content-center gap-3">
        <AppCard
          v-for="card in Cards"
          :text="card.text"
          :icon="card.icon"
          :badgeColor="card.badgeColor"
          :image="card.image"
          :title="card.title"
          :badge="card.badge"
          :author="card.author"
          :description="card.description"
        />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
