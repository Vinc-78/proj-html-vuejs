<template>

<div class="container-fluid sfondo-slider">

     <div class="slider" v-for="(ele, index) in test" :key="index">

        <div :class="indicatore===index ? 'visibile' : 'invisibile' ">

            <div class="immagine-test mb-5">

                <img  v-bind:src="require(`../assets/imgToLearning/${ele.img}`)" alt=" ">
                
            </div>

            <div class="descrizione-test mb-4">

                {{ele.descizione}}

            </div>

            <div class="nome-test mb-2">

               <h1>{{ele.nome}}</h1> 

            </div>

            <div class="ruolo-test">

                {{ele.ruolo}}

            </div>

        </div>
    </div> 

     <div class="headerChange d-flex justify-content-center align-items-center">
        <div v-for="n in 6" :key="n" 
        class=" cerchio-slide d-flex justify-content-center align-items-center" 
        @click="indicatore=(n-1)">
          {{ n.div }}
          <div class="attivo"></div>
        </div>
      </div>
  

</div>
    
</template>

<script>


export default {
    name:"Slider",

    data() {
        return {
            indicatore: 0,
            test:[
                {
                    img:"testimonials-standard-1.png",
                    nome:"Primo Levi",
                    ruolo:"Studente 1",
                    descizione: "Lorem ipsum dolor sit, amet consectetur adipisicing elit."

                },
                 {
                    img:"testimonials-standard-2.png",
                    nome:"Secondo Levi",
                    ruolo:"Studente 2",
                    descizione: "Explicabo dignissimos consectetur minima qui velit illum nisi id temporibus quidem laudantium quisquam laborum,"

                },
                {
                    img:"testimonials-standard-3.png",
                    nome:"Terzo Levi",
                    ruolo:"Studente 3",
                    descizione: "Explicabo quo cum repellat exercitationem sequi quibusdam eveniet magnam."

                },
                {
                    img:"testimonials-standard-4.png",
                    nome:"Quarto Four",
                    ruolo:"Studente 4",
                    descizione: "Lorem ipsum dolor sit, amet consectetur adipisicing elit Explicabo quo cum repellat exercitationem sequi quibusdam eveniet magnam."

                },
                 {
                    img:"testimonials-standard-5.png",
                    nome:"Quinto Five",
                    ruolo:"Studente 5",
                    descizione: "Explicabo dignissimos consectetur minima qui velit illum nisi id temporibus quidem laudantium quisquam laborum,"

                },
                {
                    img:"testimonials-standard-6.png",
                    nome:"Sesto Six",
                    ruolo:"Studente 6",
                    descizione: "Explicabo quo cum repellat exercitationem sequi quibusdam eveniet magnam."

                },
            ]

        }
    }

}


</script>

<style lang="scss">

.sfondo-slider {

    min-height: 650px;
    background-image: url("../assets/imgToLearning/h5-parallax-img-1.png");
    position: relative;
}


.immagine-test {
    height: 110px;
    width: 110px;
}

.slider {position: relative;}

.invisibile {
    display: none;
}

.visibile {
   display: flex;
   flex-direction: column;
   align-items: center;
   color: white;
   font-size: 18px;
   position: absolute;
   left:50%;
   top:50%;
   transform: translate(-50%, 50%);
  


}

.headerChange {
  position: absolute;
  bottom: 10%;
  left:-1%;
  width: 100%;
  height: 50px;
}
.cerchio-slide {
  width: 10px;
  height: 10px;
  margin: 0 5px;
  border-radius: 50%;
  background: rgb(167, 219, 242);
}

.cerchio-slide:hover .attivo {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: white;
}




</style>
