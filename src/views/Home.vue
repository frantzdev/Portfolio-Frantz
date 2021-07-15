<template>
<div>
   <Header/>
   <Carrousel/>
   <Propos/>
   <Services/>
   <Realisations/>
   <Contact/>
   <Footer/>
</div>
</template>

<script>

import Header from '../components/Header'
import Carrousel from '../components/Carrousel'
import Propos from '../components/Propos'
import Services from '../components/Services'
import Realisations from '../components/Realisations'
import Contact from '../components/Contact'
import Footer from '../components/Footer'
export default {
    name: 'Home',
    components: {
      Header, Carrousel, Propos, Services, Realisations, Contact, Footer 
    }
}
  
</script>

 <style>
  /* @keyframes describ {
    0% {
      transform: translateY(-100px);
      opacity: 0;
    }

    50% {
      transform: translateY(-50px);
      opacity: 1;
    }

    100% {
      transform: translateY(0px);
      opacity: 0;
    }

  } */
 </style>

  





