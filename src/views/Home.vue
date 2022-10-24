<template>
    <IntroductionProjet/>
    <MyTitle msg="Nos locaux"/>
    <Carousel :slides="slides"/>
  </template>
  
  <script>
  import MyTitle from '../components/composantTitle/composantTitle.vue'
  import Carousel from '../components/composantCarousel/composantCarousel.vue'
  import IntroductionProjet from '../components/composantIntroductionProjet/composantIntroductionProjet.vue'
  import photo1 from '../assets/photo1.jpg'
  import photo2 from '../assets/photo2.jpg'
  import photo3 from '../assets/photo3.jpg'
  
  
  export default {
    name: 'Home',
    components: {
      IntroductionProjet,
      MyTitle,
      Carousel
    },
    data() {
      return {
        slides: [
          photo1,
          photo2,
          photo3,
          photo2,
          photo3
      
        ]
      }
    }
  }
  </script>
  
  <style>
  
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display&display=swap');
  
  /* Scroll bar stylings */
  ::-webkit-scrollbar {
      width: 10px;
      height: 10px;
    }
  
    /* Track */
    ::-webkit-scrollbar-track {
      background: var(--lightestgrey); 
    }
    
    /* Handle */
    ::-webkit-scrollbar-thumb {
      background: rgba(187,34,179,0.5); 
      border-radius: 5px;
    }
  
    /* Handle on hover */
    ::-webkit-scrollbar-thumb:hover {
      background: rgba(187,34,179,1); 
    }
  
  html,body {
  
    margin:0;
    padding:0;
    background-color: rgb(192, 192, 192);
  
  }
  
  
  </style>
  