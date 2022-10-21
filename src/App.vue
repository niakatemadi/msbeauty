<template>
  <Navbar />
  <div class="mybg">
    <section class="presentation">
    <p>Idéalement situé à Pierrelaye, juxtaposant le bar chicha lounge O'KLM<br/> 
      l’institut BEAUTY MS vous invite à profiter d’une parenthèse de beauté<br/> 
      au sein d’un petit cocon de douceur.
    </p>
    <p>
      Nous nous ferons un véritable plaisir de vous recevoir et nous serons<br/>
      aux petits soins pour vous proposez des soins de qualités avec<br/> des produits 
      naturels et de révélez votre splendeur en vous offrant des soins dentaires 
      et du visage adaptés aux besoins de votre peau !
    </p>
    <p>Qu’attendez-vous alors pour réserver des instants uniques de beauté chez Beauty MS !</p>
    </section>
  </div>
  <HelloWorld msg="Nos locaux :"/>
  <Carousel :slides="slides"/>
  <footer class="coordonnees">
    <h1>Nos coordonnées :</h1>
    <section>
      <div class="adresse"><img src="./assets/emplacement.png"  alt="icone localisation"/> <p>85 Route d'Eragny à Bessancourt</p><p>95220 Pierrelaye</p></div>
      <div class="telephone"><img src="./assets/telephone-portable.png"  alt="icone telephone"/> <p>Appelez-nous au :</p><p>07 xx xx xx xx</p></div>
      <div class="email"><img src="./assets/email.png"  alt="icone email"/><p>Contactez-nous par email :</p><p>xxxx@gmail.com</p></div>
    </section>
  </footer>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Navbar from './components/componentNavbar/componentNavbar.vue'
import Carousel from './components/carousel/composantCarousel.vue'
import photo1 from './assets/photo1.jpg'
import photo2 from './assets/photo2.jpg'
import photo3 from './assets/photo3.jpg'


export default {
  name: 'App',
  components: {
    HelloWorld,
    Navbar,
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
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display&display=swap');

html, body {
  margin:0;
  padding:0;
  background-color: rgb(192, 192, 192);
  
  
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}
.mybg{
  background-image: url(./assets/logo.jpg);
  background-position: center center;
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: cover;
  width:100%;
  height:770px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: 'Roboto', sans-serif;
}
section.presentation{
  width : 39vw;
  height:450px;
  background-attachment: fixed;
  font-size: large;

  background-color: rgb(192, 192, 192,0.7);
  border-radius: 40px;
}
section.presentation p {
  color :rgba(187,34,179,1);
  font-weight:bold;
  margin-top:50px;
  margin-right:7px;
  margin-left: 7px;
  font-family: 'Playfair Display', serif;
  
}
footer.coordonnees{
  height:250px;
  width:100%;
  margin-top:100px;
  background: rgb(192, 192, 192);
  background: linear-gradient(180deg,rgb(192, 192, 192)  0%, rgba(187,34,179,0.8886905103838411) 90%);
}
footer.coordonnees h1 {
  color: rgba(187,34,179);
  text-decoration: underline;
  font-family: 'Playfair Display', serif;
}
footer.coordonnees section {
  display: flex;
  justify-content: space-around;
  align-items:center;
  height:180px;
}
footer.coordonnees div {
  width:200px;
  height:100px;
  font-weight: 400;
  color:white;
}
</style>
