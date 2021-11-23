<template>
  <main>
    <TopMainIcon :dataicon="icon"></TopMainIcon>

    <ToPotential></ToPotential>

    <ToLearning :datasezioni="sezioni" :datalink="links"></ToLearning>

    <PopularCourse></PopularCourse>
    
  </main>
</template>

<script>
import TopMainIcon from "./TopMainIcon.vue";
import ToPotential from "./ToPotential.vue";
import ToLearning from "./ToLearning.vue";
import PopularCourse from "./PopularCourse.vue";


export default {
  components: {
    TopMainIcon,
    ToPotential,
    ToLearning,
    PopularCourse
    
  },

  data() {
    return {
      icon: [
        {
          img: "h5-custom-icon-1.png",
          text: "Languages",
        },
        {
          img: "h5-custom-icon-2.png",
          text: "Software",
        },
        {
          img: "h5-custom-icon-3.png",
          text: "Business",
        },
        {
          img: "h5-custom-icon-4.png",
          text: "Chemistry",
        },
        {
          img: "h5-custom-icon-5.png",
          text: "Science",
        },
        {
          img: "h5-custom-icon-6.png",
          text: "DIY&Craft",
        },
      ],
      sezioni: [
        {
          titolo: "What We Do",
          status: true,
        },
        {
          titolo: "Degree Programme",
          status: false,
        },
        {
          titolo: "Career Achievements",
          status: false,
        },
        {
          titolo: "Personal Managment",
          status: false,
        },
        {
          titolo: "Steps To Success",
          status: false,
        },
        {
          titolo: "Knowledge Transfer",
          status: false,
        },
      ],
      links: [
        {
          titolo: "We enrich lives through learning.",
        },
        {
          titolo: "Maximizing potential through individual attention.",
        },
        {
          titolo: "The trusted name for specialized training.",
        },
        {
          titolo: "People thach. People learn. This is where they connect.",
        },
      ]
    };
  },
};
</script>

<style lang="scss">
</style>