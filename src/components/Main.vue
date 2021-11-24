<template>
  <main>
    <TopMainIcon :dataicon="icon"></TopMainIcon>

    <ToPotential></ToPotential>

    <ToLearning :datasezioni="sezioni" :datalink="links"></ToLearning>

    <PopularCourse :datacorsi="corsi" ></PopularCourse>

    <ToBrand 
    :datacontenuti="contenuti"
    :datapiani="piani" 
    :datacolonnaSx="colonnaSx" 
    :datacolonnaCentro="colonnaCentro"
    :datacolonnaDx="colonnaDx"
    :databrand="brand"
    > </ToBrand>
    
  </main>
</template>

<script>
import TopMainIcon from "./TopMainIcon.vue";
import ToPotential from "./ToPotential.vue";
import ToLearning from "./ToLearning.vue";
import PopularCourse from "./PopularCourse.vue";
import ToBrand from "./ToBrand.vue";


export default {
  components: {
    TopMainIcon,
    ToPotential,
    ToLearning,
    PopularCourse,
    ToBrand
    
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
      ],
      corsi: [
        {
          img: "course-5-f-img.jpg",
          professione: "Android Developer",
          nome: "David Sanders",
          descrizione:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit.!",
          titolo: "Free",
          status: true,
          genere: "Programming",
        },
        {
          img: "course-6-f-img.jpg",
          professione: "Web Designing",
          nome: "Jennifer Powell",
          descrizione:
            "Quaerat repellat libero molestiae obcaecati consequuntur laborum voluptatum, similique ipsum!",
          titolo: "Free",
          status: true,
          genere: "Programming",
        },
        {
          img: "course-12-f-img.jpg",
          professione: "Financial Modeling",
          nome: "Edward Bowman",
          descrizione:
            "Lorem ipsum dolor sit amet consectetur  laborum voluptatum, similique ipsum!",
          titolo: "$20",
          status: false,
          genere: "Business",
        },
      ],
      contenuti:[
        {
            titolo: "Number of Courses",
        },
        {
            titolo: "Time",
        },
        {
            titolo: "Web Designing",
        },
        {
            titolo: "Human-Centered Design",
        },
        {
            titolo: "Basic Marketing",
        },
        {
            titolo: "Python for Everybody",
        },
        {
            titolo: "Android Developer",
        },
        {
            titolo: "Business English",
        },
      ],
      piani:[
        {
            img : "h5-custom-icon-7.png",
            piano: 'Standard',
            price: '$12',
        },
        {
            img : "h5-custom-icon-8.png",
            piano: 'Professional',
            price: '$59',
        },
        {
            img : "h5-custom-icon-9.png",
            piano: 'Advance',
            price: '$88',
        },
    
    
      ],
      colonnaSx:[
        {
            titolo: "2",
        },
        {
            titolo: "15 Days",
        },
        {
            current: true
        },
        {
            current: true
        },
        {
            current: false
        },
        {
            current: false

        },
        {
            current: false

        },
        {
            current: false
        },
            
      ],
      colonnaCentro:[
        {
            titolo: "4",
        },
        {
            titolo: "30 Days",
        },
        {
            current: true
        },
        {
            current: true
        },
        {
            current: true
        },
        {
            current: true
        },
        {
            current: false
        },
        {
            current: false
        },
   
      ],
      colonnaDx:[
        {
            titolo: "6",
        },
        {
            titolo: "30 Days",
        },
        {
            current: true
        },
        {
            current: true
        },
        {
            current: true
        },
        {
            current: true
        },
        {
            current: true
        },
        {
            current: true
        },
        
      ],
      brand:[
        {
            img : "h5-client-5.png"
        },
        {
            img : "h5-client-1.png"
        },
        {
            img : "h5-client-2.png"
        },
        {
            img : "h5-client-1.png"
        },
    
      ]
      
    };
  },
};
</script>

<style lang="scss">
</style>