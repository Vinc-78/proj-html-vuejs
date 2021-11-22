<template>
  <main>
    <TopMainIcon :dataicon="icon"></TopMainIcon>

    <ToPotential></ToPotential>
    
  </main>
</template>

<script>
import TopMainIcon from "./TopMainIcon.vue";
import ToPotential from "./ToPotential.vue";

export default {
  components: {
    TopMainIcon,
    ToPotential,
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
    };
  },
};
</script>

<style lang="scss">
</style>