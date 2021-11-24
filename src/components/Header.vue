<template>
<header class=container-fluid >
      <div class="background">
         <div class="sfondo-opaco"></div>

          <div class="container headerTop d-flex  justify-content-between align-items-center " style="margin-left:-10px">
              <div class="logo d-flex align-items-center">
                  <img src="../assets/img/logo-light.png" alt="">
              </div>
              <nav class="link ">
                  <ul>
                    <li v-for="(link, index) in links" :key="index">
                      <a href="#">{{link.text}}</a>
                        
                    </li>
                  </ul>
              </nav>
              <div class="icone-nav-right">
                <i class="fa fa-search" aria-hidden="true"></i>
                <i class="fa fa-clipboard" aria-hidden="true"><div class="num d-flex justify-content-center align-items-center text-white"> 0 </div></i>
                <i class="fa fa-bars" aria-hidden="true"></i>

                
              </div>
          </div>
          <div class="headerCenter">
              <h1 class="HeroTitle">Contemporary Ideas</h1>
              <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. 
                  Dicta voluptate enim unde temporibus nam exercitationem nulla odit, 
                  et, accusantium eveniet adipisci! At nesciunt repudiandae ex 
                  accusantium laudantium voluptatem, eius ipsum.
                  </p>


              <div class="registrati">
                
                  <p class="registrati-ora"><a href="#">Register Now</a> </p>
                
              </div>
          </div>

          <div class="headerChange d-flex justify-content-center align-items-center">
              <div v-for="n in 3" :key="n" class="cerchio d-flex justify-content-center align-items-center">
                  {{n.cerchio}}
                  <div class="attivo"></div>
              </div>
          </div>
      </div>
  </header>   


    
</template>


<script>
export default {
  name: 'Header',
  data() {
    return {
      links: [
        {
          text: "Home",
          url: "#",
        },
        {
          text: "Courses",
          url: "#",
        },
        {
          text: "Istructor",
          url: "#",
        },
        {
          text: "Events",
          url: "#",
        },
        {
          text: "Pages",
          url: "#",
        },
        {
          text: "Elements",
          url: "#",
        },
      ]
    }
  }
}
</script>

<style  lang="scss">
@import "../styles/variabili.scss";


.background {
    position: relative;
    width: 100%;
    height: 600px;
    background-image: url('../assets/img/course-9-f-img.jpg');
    background-repeat: no-repeat;
    background-size: cover;
  }


.sfondo-opaco {
    position: absolute;
    width: 100%;
    height: 100%;
    background: rgb(5, 5, 5, 0.3);
  }

  .headerTop {
    position: absolute;
    left: 50%;
    transform: translate(-50%);
    height: 90px;
    

  }

  .logo {
   width: 200px;
    
  }

  .logo > img {
    width: 100%;
  }

  .link{padding-top: 15px;}

  ul, li {
    width: 100%;
    display: flex;
    list-style: none;
    margin: 20px;
    list-style-type: none;
    
    
    a {text-decoration: none;
       font-size: 20px;
       color: white;}

    a:hover {color:white;}
  }

  .icone-nav-right {
    text-align: end;
    width: 200px;
    margin:0 20px;
    font-size: 25px;
    
  }

  .fa {
    margin-right: 20px;
    color: white
  }

  .fa-clipboard { position: relative;}

  .num {
  position: absolute;
  top: 0;
  right: 0;
  transform: translate(60%, -20%);
  width: 15px;
  height: 15px;
  border-radius: 50%;
  background: $celestino;
  font-size: 12px;
  
}

.headerCenter {
    position: absolute;
    width: 80%;
    margin: 0 auto;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;

    .HeroTitle{ font-size: 70px;}

    h1,
     p {
    color: white;
    padding: 15px;
  }
  }

  
 .registrati {
    position: relative;
    width: 200px;
    height: 80px;
    margin: 0px auto;
    text-transform: uppercase;
    background: $celestino;
    color: white
  }

  .registrati-ora {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 100%;
    font-size: 20px;

    a {text-decoration: none;
      color: white;}
  }

  .headerChange {
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 50px;
    
  }
  .cerchio {
    width: 20px;
    height: 20px;
    margin: 0 5px;
    border-radius: 50%;
    border: 2px solid grey;
    background: grey;
    
    
  }
  
  .cerchio:hover .attivo{
     width: 10px;
    height: 10px;
    border-radius: 50%;
    background: white;
    
    
  }
 
  .cerchio:hover { border:1px solid white;}
  

</style>