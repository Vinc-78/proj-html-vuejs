<template>
  <section class="ToBrand">

      <div class="container-fluid my-5  shell-course">
        <div class="container pianiMain border-bottom">

           <div class="GoTop d-flex flex-column justify-content-center align-items-center "  style="bottom: 42%; right:-1%; z-index: 2;">
                <i class="fa fa-angle-up" aria-hidden="true"></i>
                <a href="#">TOP</a>
            </div>

          <div class="plans d-flex flex-column justify-content-center align-items-center">
              
            <div class="plans-titolo">
                <h1 >Pricing Plans</h1>
                <p class="my-3 fs-5 text-secondary">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo enim quaerat temporibus 
                  
                  </p>
            </div>
            <div class="partecentrale container d-flex">
                    <!-- Elenco di sinistra -->
                <div class="left">

                <div class="boxTop">
                    <p class="save">Save up to 40% by paying weekly</p>
                </div>
                <div class="boxCella">
                    <div v-for="(cell, index) in datacontenuti" :key="index" class="cella">
                    <p class="titolo">{{cell.titolo}}</p>
                    </div>
                </div>
                </div>
                    <!-- Struttura di destra -->
                <div class="right">
                        <!-- Immagini  -->
                    <div class="boxsTop">
                        <div v-for="(p, index) in datapiani" :key="index" class="tipiDiPiani
                        d-flex flex-column justify-content-center align-items-center">

                        <img :src="require(`../assets/imgToBrand/${p.img}`)" alt="">
                        <h3 class="piano"> {{p.piano}} </h3>
                        <p class="sottoColonna"> {{p.price}} </p>
                        </div>
                    </div>
                     <!-- Tabella  -->
                    <div class="containerBox">

                        <div class="boxContainer">

                            <div v-for="(cell, index) in datacolonnaSx" :key="index" class="righe">
                                <p class="testi">
                                {{cell.titolo}} <i :class="(cell.current) ? 'fa fa-check spunta' : 'fa fa-times noX'"></i>
                                </p>
                            
                            </div>
                            <div class="getItNow d-flex justify-content-center align-items-center">
                                <p class="getItNowTesto d-flex justify-content-center align-items-center">
                                    GET IT NOW</p>
                            </div>

                        </div>

                        <div class="boxContainer">
                            <div v-for="(cell, index) in datacolonnaCentro" :key="index" class="righe">
                                <p class="testi">
                                {{cell.titolo}} <i :class="(cell.current) ? 'fa fa-check spunta' : 'fa fa-times noX'"></i>
                                </p>
                            </div>

                            <div class="getItNow d-flex justify-content-center align-items-center">
                                <p class="getItNowTesto d-flex justify-content-center align-items-center">
                                    GET IT NOW</p>
                            </div>
                        </div>

                        <div class="boxContainer">
                            <div v-for="(cell, index) in datacolonnaDx" :key="index" class="righe">
                                <p class="testi">
                                {{cell.titolo}} <i :class="(cell.current) ? 'fa fa-check spunta' : 'fa fa-times noX'"></i>  
                                </p>
                                <!-- <i :class="(tab.current) ? 'fas fa-check' : 'fas fa-times'"></i> -->
                            </div>
                            <div class="getItNow d-flex justify-content-center align-items-center">
                                
                                <p class="getItNowTesto d-flex justify-content-center align-items-center">
                                    GET IT NOW</p>
                            </div>
                        </div>

                    </div>
                </div>

            </div>

          </div>

      </div>

      </div>

      

      <div class="container-fluid brand pb-5">

        <div class="loghibrand d-flex align-items-center justify-content-center" >
         
          <div v-for="(img, index) in databrand" :key="index" class="loghi">
            <img class="w-100" :src="require(`../assets/imgToBrand/${img.img}`)" alt="">
          </div>
        </div>  

      </div>

  

  </section>
</template>

<script >
export default {
  noma: "ToBrand",

  props:{

        datacontenuti: Array,
        datapiani: Array,
        datacolonnaSx: Array,
        datacolonnaCentro: Array,
        datacolonnaDx: Array,
        databrand: Array

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

.pianiMain{ position: relative;}

.plans {
  margin: 30px 0px;
  padding: 100px 0px;
  width: 100%;
  height: 100%;
  
  
}
.plans-titolo {
  width: 70%;
  margin: 50px auto;
  text-align: center;
}


.left {
  width: 30%;
}
.right {
  position: relative;
  width: 70%;
}

.boxTop {
  position: relative;
  width: 100%;
  height: 275px;
  border: 1px solid #EAEAEA;
  border-top: 5px solid #D6F2FF;
}
.save {
  position: absolute;
  top: 35%;
  left: 50%;
  transform: translate(-50%);
  font-size: 30px;
  font-weight: bold;
  color:#3E3E3E;
  font-size:25px;
}
.piano {
  margin: 30px;
  font-weight: bold;
  color: #3E3E3E;
  font-size:25px;
}
.sottoColonna {
  font-weight: bold;
  color: #545454;
}
.boxCella {
  width: 100%;
  height: calc(100% - 300px);
}
.cella {
  position: relative;
  width: 100%;
  height: 50px;
  border: 1px solid  #EAEAEA;
  color: #B9B9B9;
  font-weight: bold;
  background-color: white;
}
.titolo {
  position: absolute;
  top: 50%;
  left: 25%;
  transform: translate(0%, -50%);
}
.boxsTop {
  width: 100%;
  height: 275px;
  display: flex;
  background: #F2F8FC;
}
.tipiDiPiani {
  width: calc(100% / 3);
  height: 275px;
  border: 1px solid  #EAEAEA;
  border-top: 5px solid #D6F2FF;
  
}
.containerBox {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: calc(100% - 275px);
  display: flex;
}
.boxContainer {
  width: calc(100% / 3);
  height: calc(100% - 50px);
}
.righe {
  width: 100%;
  height: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid #EAEAEA;
  color: #B9B9B9;
  font-size: 18px!important;
  background-color: white;
}

.spunta{ color:$celestino;}

.noX {color:#B9B9B9;}


.testi {
  margin: 50% auto;
}
.getItNow {
  width: 100%;
  height: 90px;
  border: 1px solid #EAEAEA;
  background: #F2F8FC;
  
}
.getItNowTesto {
  margin: 50% auto;
  width: 60%;
  height: 70%;
  border: 1px solid #EAEAEA;
  font-weight: bolder;
  color: #b9b9b9;
  background-color: white;

  &:hover {background-color: $celestino;
           color:white;}
  
}




</style>
