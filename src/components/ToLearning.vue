<template>
  <section>

    <div class="shell container-fluid border-bottom">

      <div class=" testimonials  d-flex flex-column justify-content-center align-items-center ">

      

      <div class="testimonial container">

      
          <div class="immagine-testimonial text-center">

              <img  class="w-100 " src="../assets/imgToLearning/testimonials-standard-2.png" alt=""  />

          </div>
        
      </div>

      <div class="descrizione text-white text-center">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Minus, amet
          nesciunt itaque inventore error, quod laboriosam voluptates sunt
          numquam aperiam autem dolorem dolorum maxime eligendi. Earum nemo a
          explicabo placeat!
        </p>

        <h3>Joan Collins</h3>
        <h6 class="my-2">STUDENT</h6>
      </div>

      <div class="headerChange d-flex justify-content-center align-items-center">
        <div v-for="n in 3" :key="n" class=" cerchio-azzurro d-flex justify-content-center align-items-center" >
          {{ n.div }}
          <div class="attivo"></div>
        </div>
      </div>
      </div>

         <div class="container">

            <div class="row box-learning my-5">

              <div class="GoTop d-flex flex-column justify-content-center align-items-center " style="bottom: -20%">
              <i class="fa fa-angle-up" aria-hidden="true"></i>
              <a href="#">TOP</a>
               </div>


      <div class="col-4 aside">
        <div
          v-for="(sezione, index) in datasezioni"
          :key="index"
          class="aside-line d-flex justify-content-start align-items-center"
        >
          <div :class="sezione.status ? 'attiva, altro' : null"></div>
          <p style="margin-bottom: 0 !important" class="aside-title">
            {{ sezione.titolo }}
          </p>
        </div>
      </div>

      <div class="col-8">

        <div class="learning d-flex flex-column ">
          <h1>Learning Possibilities</h1>
          <p class="my-5">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed cumque
            libero itaque adipisci explicabo atque deleniti, molestiae corrupti,
            architecto omnis, assumenda tempore iure qui sapiente suscipit!
            Numquam dignissimos explicabo dolor!
          </p>

          <ul class=" lista-link-learning d-flex flex-column mt-5" >
            <li v-for="(link, index) in datalink" :key="index" class="nav my-2 flex-nowrap align-items-center">
              <i class="fa fa-check" aria-hidden="true"></i>
              {{ link.titolo }}
            </li>
          </ul>

          <div class="icona">
            <img
              class="w-75"
              src="../assets/imgToLearning/h12-tabs-icon-1.png"
              alt=""
            />
          </div>
        </div>
      </div>
            </div>
        </div>
    </div>

  </section>
</template>

<script >
export default {
  noma: "ToLearning",

  props:{

        datasezioni: {Array},
        datalink: {Array}

    },

 
};
</script>

<style lang="scss">
@import "../styles/variabili.scss";

.testimonials {
  height: 600px;
  width: 100%;
  background-image: url("../assets/imgToLearning/h5-parallax-img-1.png");
  background-repeat: no-repeat;
  background-size: 200%;
  background-position: top, bottom;
  position: relative;
}

.testimonial {
  width: 100px;
  height: 100px;
  position: relative;

  .immagine-testimonial {
      position: absolute;
      top:0;
      left:50%;
      transform:translate(-50%,-50%)
  }
}

.descrizione {
  p {
    margin: 25px 20%;
  }
}

.box-learning {
  height: 700px;
}

.aside-line {
  width: 100%;
  height: 100px;
  border: 1px solid rgb(41, 40, 40);

  :hover,
  .attiva {
    color: $celestino;
    border-left: 10px solid $celestino;
    height: 100%;
    padding-left: 20px;
    display: flex;
    align-items: center;
  }
}

.aside-title {
  padding-left: 30px;
  color: rgb(132, 123, 123);
  font-size: 24px;
  font-weight: bolder;
}

.learning {
  position: relative;
  width: 80%;
  height: 90%;
  margin: 0 auto;

  h1 {
    font-size: 50px;
  }

  p {
    
    color: rgb(173, 173, 173);
    font-size: 20px;
  }

  .icona {
    position: absolute;
    bottom: 5%;
    right: -15%;
  }
}

.lista-link-learning {
  margin-left: -20px !important;
  width: 75%;

  .nav {
    margin: 5px 0;
    list-style: none;
    color: rgb(173, 173, 173);
    font-size: 20px;
  }

  .fa-check {
    color: $celestino;
    font-size: 18px;
  }
}

.headerChange {
  position: absolute;
  bottom: 10%;
  width: 100%;
  height: 50px;
}
.cerchio-azzurro {
  width: 10px;
  height: 10px;
  margin: 0 5px;
  border-radius: 50%;
  background: rgb(167, 219, 242);
}

.cerchio-azzurro:hover .attivo {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: white;
}
</style>
