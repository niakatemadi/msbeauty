<template>
    <div class="SectionIntroductionProjet">
    <section class="SectionIntroductionProjet-presentation">
    <p>Idéalement situé à Pierrelaye
      l’institut BEAUTY MS vous invite à profiter d’une parenthèse de beauté
      au sein d’un petit cocon de douceur.
    </p>
    <p>
      Nous nous ferons un véritable plaisir de vous recevoir et nous serons<br/>
      aux petits soins pour vous proposez des services de qualités avec<br/> des produits 
      naturels et de révélez votre splendeur en vous offrant des soins adaptés à vos besoins !
    </p>
    <p>Qu’attendez-vous alors pour réserver des instants uniques de beauté chez Beauty MS !</p>
    </section>
  </div>
</template>

<style scoped>
.SectionIntroductionProjet{
  background-image: url(../../assets/logo.jpg);
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
.SectionIntroductionProjet-presentation{
  width : 39vw;
  width : 600px;
  background-attachment: fixed;
  font-size: large;
  background-color: rgb(192, 192, 192,0.8);
  border-radius: 40px;
}
.SectionIntroductionProjet-presentation p {
  color :black;
  font-weight:bold;
  margin-top:50px;
  margin-right:7px;
  margin-left: 7px;
  font-family: 'Playfair Display', serif;
  text-align:center;
  
}
@media screen and (max-width : 650px){
    .SectionIntroductionProjet-presentation{
        width : 450px;
        height: auto;
    }
}
@media screen and (max-width : 560px){
    .SectionIntroductionProjet-presentation{
        width : 350px;
        height: auto;
    }
}
@media screen and (max-width : 380px){
    .SectionIntroductionProjet-presentation{
        margin-top : 50px;
        width : 300px;
        height: auto;
    }
}
</style>
