<template>
      <header class="Header">
        <nav class="Header-navbar" :class="displayNav ? 'yes' : ''">
          <div>
            <h1 class="Header-title"><router-link to="/">BEAUTY MS</router-link></h1>
          </div>
          <div class="Header-toggleButton" @click="displaynav">
            <span class="bar1"></span>
            <span class="bar2"></span>
            <span class="bar3"></span>
          </div>
          <ul class="Header-blocNavigation">
            <li><router-link to="/">Accueil</router-link></li>
            <li>  <router-link to="/prestations">Prestations</router-link></li>
            <div class="Header-logo">
                <li class="Header-instagramButton"> <a href="https://www.instagram.com/beauty.ms_95/?hl=fr" target="_blank"><img src="./assets/instagram1.png"  alt="Logo instagram"/></a></li>
                <li class="Header-snapchatButton"> <a href="" target="_blank"><img src="./assets/snapchat.png"  alt="Logo snapchat"/></a></li>
            </div>
          </ul>
        </nav>
      </header>
      <RouterView/>
      <footer class="Footer">
    <h1 class="Footer-title">Nos coordonnées </h1>
    <section>
      <div><img src="./assets/emplacement.png"  alt="icone localisation"/> <p>85 Route d'Eragny à Bessancourt</p><p>95220 Pierrelaye</p></div>
      <div><img src="./assets/telephone-portable.png"  alt="icone telephone"/> <p>Appelez-nous au :</p><p>07 66 22 04 25</p></div>
      <div><img src="./assets/email.png"  alt="icone email"/><p>Contactez-nous par email :</p><p>xxxx@gmail.com</p></div>
    </section>
  </footer>
</template>

<script>
import { RouterView } from 'vue-router';

  export default {
    name: "navBar",
    data() {
        return {
            displayNav: false,
            isInputFocused: false,
        };
    },
    methods: {
        displaynav() {
            this.displayNav = !this.displayNav;
        }
    },
    components: { RouterView }
};
  </script>
  <style scoped>

.Header 
{
    top: 0px;
    left: 0px;
    width: 97%;
    padding: 0 2rem;
    background-color: rgba(192, 192, 192,1);
    color:rgba(187, 34, 179,1) ;
    height: 9vh;
    position: fixed;
    z-index: 99;
    font-weight: bold;
    font-family: 'Playfair Display', serif;

}
.Header-navbar 
{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    height: 100%;
    width: 100%;
    border-bottom: 1px solid rgba(187, 34, 179,1);
}
.Header-logo {
    display: flex;
    flex-direction: row;
}
.Header-logo li {
    margin : 5px;
}
.Header-title
{
    font-size: 2.5em;
    background-color: rgba(187, 34, 179,0);
    text-decoration: overline;
}
.Header-title a {
    color : rgba(187, 34, 179,1);
    text-decoration: none;
}
.Header-blocNavigation
{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    width: 30rem;
    list-style: none;
    font-size: 1.1em;
    color:rgb(0, 0, 0)!important;
}
.Header-toggleButton
{
    display: none;
    width:40px;
    height:40px;
}
.Header-toggleButton:hover 
{
    cursor: pointer;
}
.Header-blocNavigation li:hover 
{
    cursor: pointer;
    transform: scale(1.05);
    text-decoration: underline;
    transition: 0.3s;
}
.Header-blocNavigation a
{
    text-decoration: none;
    color : rgba(187, 34, 179,1);
}
.Header-instagramButton:hover
{
    opacity: 0.8;
    transform: scale(1);
}

@media screen and (max-width : 768px){
    .Header-title
    {
        display: block;
        position: relative;
        z-index: 30;
    }
    .Header-logo {
    display: flex;
    flex-direction: column;

    }
    .Header-toggleButton 
    {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        position: relative;
        right: 3rem;
        z-index: 30;
        font-size: 2em;
    }
    .bar1,.bar2,.bar3 {
    display: inline-block;
    width: 40px;
    height:5px;
    background-color: rgba(187, 34, 179,1);
    border-radius : 5px;
    }
    .yes .bar1,.bar2{
        position: absolute;
        top:17px;
    }
    .yes .bar2{
        transform: rotateZ(45deg);
    }
    .yes .bar1{
        transform: rotateZ(-45deg);
    }
    .yes .bar3 {
        display: none;
    }
    .yes .Header-blocNavigation
    {
        transform: translateX(0%);
    }
    .Header-blocNavigation
    {
        position: absolute;
        top: 58px;
        left: 0px;
        width: 90%;
        height: 30vh;
        background-color: rgb(187, 34, 179);
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        transform: translateX(-100%);
        transition: 0.3s ease-in;
        padding-left: 0;
    }
    .Header-blocNavigation a
    {
        text-decoration: none;
        color : white;
    }
    .Header-blocNavigation li
    {
        text-decoration: none;
        transform : scale(1.5);
    }
}

.Footer{
  width:100%;
  margin-top:100px;
  color: rgba(187,34,179);
  background: rgb(192, 192, 192);
  background: linear-gradient(180deg,rgb(192, 192, 192)  0%, rgba(187, 34, 179, 0.889) 90%);
  text-align:center;
  font-family: 'Playfair Display', serif;
}

/*Footer css*/ 
.Footer section {
  display: flex;
  flex-flow:wrap;
  justify-content: space-around;
  align-items:center;
  height:180px;
}
.Footer div {
  width:200px;
  height:100px;
  font-weight: 400;
  color:white;
}

@media screen and (max-width : 610px){
    .Footer section {
        height: 500px;
    }
}
  </style>
  