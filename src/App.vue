<template>
  <div id="app">
    
<Header></Header>
<Main></Main>
<Footer></Footer>
<Slider></Slider>

  </div>
</template>

<script>
import Header from "./components/Header.vue"
import Main from "./components/Main.vue"
import Footer from "./components/Footer.vue"
import Slider from "./components/Slider.vue"

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
    Slider
    
  }
}
</script>

<style lang="scss">
@import "@/styles/generale.scss";


</style>
