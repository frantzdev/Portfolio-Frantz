<template>
<div>
   <Header/>
   <Carrousel/>
   <Contact/>
   <Footer/>
</div>
</template>

<script>

import Header from '../components/Header'
import Carrousel from '../components/Carrousel'
import Contact from '../components/Contact'
import Footer from '../components/Footer'
export default {
    name: 'Home',
    components: {
      Header, Carrousel, Contact, Footer 
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

  





