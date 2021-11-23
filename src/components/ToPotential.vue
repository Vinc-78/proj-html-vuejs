<template>
  <section class="container">
    <div class="titolo">
      <h1 class="py-3">
        The Trusted Name <br />
        for In-Home Tutoring.
      </h1>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Odio doloribus
        quia voluptas a repellat quis labore et assumenda sint provident! Fugit
        debitis harum perspiciatis quis numquam est voluptatem assumenda amet.
      </p>

      <a href="#" class="learn-more fw-bolder fs-6 mt-3">LEARN MORE</a>
    </div>

    <div class="jumbotron">
      <img class="w-100" src="../assets/imgToPotential/h5-img-1.jpg" alt="" />

      <div class="GoTop d-flex flex-column justify-content-center align-items-center">
        <i class="fa fa-angle-up" aria-hidden="true"></i>
        <a href="#">TOP</a>
      </div>
    </div>

    <div class="to-mondo">

      <div class="GoTop d-flex flex-column justify-content-center align-items-center" style="bottom: 0;">
        <i class="fa fa-angle-up" aria-hidden="true"></i>
        <a href="#">TOP</a>
      </div>

      <div class="d-flex  align-items-center">

        <div class="mappamondo d-flex align-items-end justify-content-center">
          <img class="w-100" src="../assets/imgToPotential/h5-img-2.jpg" alt="" />
        </div>

        <div class="empowering">

          <h1 class="pt-3">
            Empowering <br />
            Children to Reach <br />
            Their Potential
          </h1>
          <p  class="pt-3">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Commodi
            inventore ipsum quam iusto? Cumque dolor neque rem, non impedit unde
            expedita. Molestiae, quas ullam? Aliquid, velit. Quo similique esse
            aliquam!
          </p>

          <div class="number-user-event d-flex ">
            <div>
              <p class="number">168</p>
              <p class="label">User Stories</p>
            </div>
            <div class="events">
              <p class="number" >347</p>
              <p class="label">Events</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script >
export default {
  noma: "ToPotential",
};
</script>

<style lang="scss">
@import "../styles/variabili.scss";


.learn-more {
    text-decoration: none;
    margin-top: 25px;
    color:$celestino;
    font-size: 18px;

}

.jumbotron {
  width: 95%;
  width: 100%;
  text-align: center;
  margin: 0 auto;
  position: relative;

  
}



  .to-mondo {
      position: relative;
      margin: 50px auto;
      width: 100%;
  

  }

  .mappamondo {
            width: 50%;
  }

  .empowering {
      width: 45%;
      padding: 25px;

      h1{
          font-size: 55px;
          margin-top:-30px; 
      }

  }

  .number-user-event {

      .label { font-size: 25px;}

      .number{ font-size: 50px;
               font-weight: bolder;}
      p {
          color:$celestino;

      }
      .events{ margin-left: 35%;}
  }

  





</style>
