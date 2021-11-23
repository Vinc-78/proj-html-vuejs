<template>
  <section class="container-fluid my-5 border-bottom shell-course">

    <div  class=" container corsi-popolari d-flex flex-column justify-content-center align-items-center " >
      <div
        class="GoTop d-flex flex-column justify-content-center align-items-center "  style="bottom: -8%; right:-1%; z-index: 2;">
        <i class="fa fa-angle-up" aria-hidden="true"></i>
        <a href="#">TOP</a>
      </div>

      <div
        class=" Popular-Online-Courses d-flex flex-column justify-content-center align-items-center " >
        <div class="titolo-corsi">
          <h1>Popular Online Courses</h1>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat
            repellat libero molestiae obcaecati consequuntur laborum voluptatum,
            similique ipsum! Rerum ut facilis quis mollitia quasi facere illum
            dignissimos saepe dolorum fuga?
          </p>
        </div>

        <div class="row row-cols-3">
          <div v-for="(img, index) in corsi" :key="index" class="col">
            <div class="col-img">
              <img
                class="w-100"
                :src="require(`../assets/imgPopularCourses/${img.img}`)"
                alt=""
              />
            </div>

            <div class="box-descrizione">
              <div
                class="fasciaRiferimento d-flex align-items-center justify-content-between " >
                <h3 class="fw-bold" style="color: #b9b9b9">
                  {{ img.professione }}
                </h3>
                <div
                  :class="img.status ? 'active' : null"
                  class=" prezzo d-flex justify-content-center align-items-center " >
                  {{ img.titolo }}
                </div>
              </div>

              <p class="nome">{{ img.nome }}</p>
              <p class="descizione-corso">{{ img.descrizione }}</p>
              <p class="descrizione-corso">
                <i class="fa fa-user fa-course" style="color:#b9b9b9;" aria-hidden="true"></i> 1
                <i class="fa fa-tag fa-course" style="color:#b9b9b9;" aria-hidden="true"></i> {{ img.genere }}
              </p>
            </div>
          </div>
        </div>

        <div
          class="headerChange-corsi d-flex justify-content-center align-items-center"  >
          <div v-for="n in 3" :key="n" class="cerchio-corso d-flex justify-content-center align-items-center ">
            {{ n.div }}
            <div class="attivo"></div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script >
export default {
  noma: "PopularCourse",

  data() {
    return {
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
    };
  },
};
</script>

<style lang="scss">
@import "../styles/variabili.scss";

.shell-course { 
   background-image: url("../assets/imgPopularCourses/page-background-img.png");
   background-size: 200%;
   min-height: 1100px;
}

.container{ position: relative;}

.Popular-Online-Courses {
  
  top: 0px;
  padding-top: 100px;
  width: 100%;
  height: 100%;
}

.titolo-corsi {
  width: 70%;
  margin: 50px auto;
  text-align: center;

  h1 {
    margin-bottom: 20px;
    font-size: 50px;
  }

  p {
    font-size: 20px;
    margin-bottom: 25px;
  }
}

.box-descrizione {
  padding: 15px;
  height: 250px;
  border: 1px solid rgb(206, 206, 206);
  position: relative;
  background-color: white;
  z-index: 1;
  
}

.fasciaRiferimento {
  .active {
    height: 100%;
    background: #ffd740;
  }
}

.nome {
  margin-top: 5px;
  color: #cecece;
  font-size: 15px;
}

.descrizione-corso {
  margin-bottom: 20px;
  color: #b9b9b9;
  font-size: 18px;
  font-weight: bolder;
  position: absolute;
  bottom: 0;
  left:5%;

  .fa-course { 
      margin-right:5px;}
 
}

.prezzo {
  width: 50px;
  height: 100%;
  border-radius: 20px;
  padding: 2px;
  background: $celestino;
  color: white;
  font-size: 14px;
}

.headerChange-corsi {
  position: absolute;
  bottom: -15%;
  width: 100%;
  height: 50px;
}
.cerchio-corso {
  width: 10px;
  height: 10px;
  margin: 0 5px;
  border-radius: 50%;
  background: rgb(167, 219, 242);
}

.cerchio-corso:hover .attivo {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: rgb(64, 196, 255);
}
</style>
