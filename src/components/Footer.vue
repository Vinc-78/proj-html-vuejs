<template>

<footer class="container-fluid">

  <div class="container linkFooter row py-5 border-bottom border-secondary " style="margin-left:150px">

    <div class="col left-link py-5">

       <div class="logoFooter py-5">
            <img class="w-100" src="../assets/imgFooter/footer-logo-1.png" alt=""/>
       </div>

       <ul class=" d-flex flex-column  py-5" >
            <li v-for="(link, index) in leftLink" :key="index" > <a href="#">{{ link.linkL }}</a>   </li>
       </ul>

       <div class="telphone d-flex py-4">
         <i class="fa fs-4 fa-phone flex-nowrap align-items-center "></i>
         <span>1-677-124-44227</span>
       </div>

       <div class="timeOpen d-flex py-2">
         <i class="fa fs-4 fa-clock-o flex-nowrap align-items-center "></i>
         <span>Mon - Sat 8.00 - 18:00</span>
       </div>

    </div>

    <div class="col central-link  py-5">

      <h1 class="py-5 text-white" style="margin-left:10px">Popular Course</h1>

      <ul class=" d-flex flex-column  " v-for="(link, index) in centralLink" :key="index" >
            <li> <h3 class="pt-5">{{ link.ruolo}}</h3></li>
            <li > <a class="link-central-name" href="#">{{ link.nome }}</a>   </li>
       </ul>


    </div>

    <div class="col right-link py-5">
      <h1 class="ps-5 py-5 text-white" style="margin-left:10px; ">Support</h1>

      <ul class=" d-flex flex-column  pt-1 " v-for="(link, index) in rightLink" :key="index" >
           <li > <a href="#">{{ link.linkR }}</a>   </li>
       </ul>

    </div>

    <div class="col world-img text-white py-5 ms-4">

      <h2 class="py-5">Flexible Learning</h2>

      <div class="MondoFooter py-5">
            <img class="w-100" src="../assets/imgFooter/footer-img-1.png" alt=""/>
       </div>

    </div>

  </div>

  <div class="container copyright d-flex justify-content-between">

    <div class="copy-left">
      <span>Copyright 2017 ©Mikado Themes</span>
    </div>

    <div class="copy-right">
      <span>Call +44 300 303 0266 </span>
      <span>FOLLOW US</span>
      <span><i class="fa fa-twitter" ></i></span>
      <span><i class="fa fa-instagram" ></i></span>
      <span><i class="fa fa-facebook" ></i></span>

    </div>


  </div>


</footer>


    
</template>


<script>
export default {
  name: 'Footer',
  data() {
    return {

      leftLink:[
        {
          linkL: "Providing Life Changing",
          url: "#",
        },
        {
          linkL: "Experiences Through",
          url: "#",
        },
        {
          linkL: "Education Class That Fit your",
          url: "#",
        },
        {
          linkL: "Busy life. closer to home",
          url: "#",
        }
      ],
      centralLink:[
          
        {
          ruolo: "Business English",
          nome: "Preston Marshall",
        },
        {
          ruolo: "Social Computing",
          nome: "David Sanders",
        },
        {
          ruolo: "Learn Spanish",
          nome: "Jennie King",
        },
      
      ],
      rightLink:[
        {
          linkR: "User dashboard",
        },
        {
          linkR: "Contact Us",
        },
        {
          linkR: "FAQ",
        },
        {
          linkR: "Course Offer",
        },
        {
          linkR: "Events",
        },
      ]
    }
  }
}
</script>

<style  lang="scss">
@import "../styles/variabili.scss";

footer{

    background-color: rgb(34, 34, 34);
    min-height: 800px;
    color:rgb(206, 206, 206)
}

.linkFooter {

  

  li{font-size:18px}
  a { text-decoration: none;
      ;

      &:hover {color:$celestino;}
  }

  

  .fa {
    color:rgb(206, 206, 206);
  }
  
}

.left-link {

  width: 140%;

  ul {  margin: -20px 0px 0px -30px;

    li {list-style-type: none;}

  }
}

.central-link {
  ul { margin: -20px 0px 0px -30px;}
  
  .link-central-name{ margin:-35px 0}

  
}

.right-link {
      h1{
        margin-bottom: 50px;
      }
      
      li { 
        margin-top: -5px;
      }
  
}

.copyright {
  padding: 50px;

  .copy-right {
    span {
      margin-left:15px;
    }

    .fa {
      font-size: 20px;
    }

    
  }
}

</style>