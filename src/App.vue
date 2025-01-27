<script>

import Header from './components/Header.vue'
import Home from './components/views/Home.vue';
import Questions from './components/Questions.vue';
import Impact from './components/views/Impact.vue';
import Testimonios from './components/Testimonios.vue';
// import Cards from './components/views/Cards.vue';
// import Services from './components/views/Services.vue';
// import Tables from './components/views/Tables.vue';

// import Prices from './components/views/Prices.vue';
import Footer from './components/views/Footer.vue';
export default {
  name: 'app',
  components: {
    Header,
    Home,
    Questions,
    Impact,
    Testimonios,
    Footer,
  }
}
</script>
<template>
   
   <div id="app" class="font-inter tracking-wide">
    <Header/>
    <Home/>
    <Questions/>
    <Impact/>
    <Testimonios/>
    <Footer/>
   </div>
</template>

