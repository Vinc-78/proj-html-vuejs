<template>

<div class="container iconList my-5">
      
      <div class="row row-cols-6 justify-content-between gy-5">

        <div v-for="(icon, i) in dataicon" :key="'Icon'+ i" 
        class="col bgicon d-flex flex-column align-items-center justify-content-center">
          <img :src="require(`../assets/imgMainTop/${icon.img}`)" alt="">
          <h4 class="mt-3"> {{icon.text}} </h4>
        </div>
      </div>

</div>



    
</template>

<script >


export default {
    noma:"TopMainIcon",

    props:{

        dataicon: {Array}

    }

}

</script>

<style lang="scss">
@import "../styles/variabili.scss";



.bgicon {
    background-color: $iconMainbg;
    height: 225px;
    width: 175px!important; 
    
    img {
        width: 50%;

        }

    &:hover {background-color: rgb(163, 252, 225);
             color:rgb(255, 255, 255);}

    
}


</style>
