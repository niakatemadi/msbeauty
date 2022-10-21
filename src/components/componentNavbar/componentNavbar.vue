<template>
    <header>
        <nav class="navbarisopen" :class="displayNav ? 'yes' : ''">
          <div class="bloc_myname">
            <h1><mark>BEAUTY MS</mark></h1>
          </div>
          <div class="togglebutton" @click="displaynav">
            <span class="bar1"></span>
            <span class="bar2"></span>
            <span class="bar3"></span>
          </div>
          <ul class="list_header_navbar">
            <li><a class="page_accueil" href="../index.html#ancre_top_accueil">Accueil</a></li>
            <li><a class="page_veille" href="../pageVeilleTechnologique/veille.html">Prestations</a></li>
            <li class="social_liste"> <a href="https://www.instagram.com/beauty.ms_95/?hl=fr" target="_blank"><img src="../../assets/instagram1.png"  alt="Logo instagram"/></a></li>
          </ul>
        </nav>
      </header>
  </template>
  
  <script>

  export default {
    name: 'navBar',
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
  };
  </script>
  <style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Shalimar&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400&family=Shalimar&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600&family=Shalimar&family=Space+Grotesk&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Comforter+Brush&family=Dancing+Script:wght@600&family=Shalimar&family=Space+Grotesk&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Comforter+Brush&family=Dancing+Script:wght@600&family=Didact+Gothic&family=Shalimar&family=Space+Grotesk&display=swap');
  header 
{
    top: 0px;
    left: 0px;
    width: 95%;
    padding: 0 2rem;
    background-color: rgba(187, 34, 179,0);
    color:rgba(187, 34, 179,1) ;
    height: 9vh;
    position: fixed;
    z-index: 99;
    font-weight: bold;

}
mark{
    font-family: 'Shalimar', cursive;
    background-color: rgba(187, 34, 179,0);
    color:rgba(187, 34, 179,1);
    text-decoration: overline;
}
nav 
{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    height: 100%;
    width: 100%;
    border-bottom: 1px solid rgba(187, 34, 179,1);
}
div.bloc_myname h1 
{
    font-size: 2.5em;
}
ul.list_header_navbar 
{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    width: 30rem;
    list-style: none;
    font-size: 1.1em;
    color:rgba(187, 34, 179,1);
}
.togglebutton 
{
    display: none;
    width:40px;
    height:40px;
}
.togglebutton:hover 
{
    cursor: pointer;
}
ul.list_header_navbar li:hover 
{
    cursor: pointer;
    transform: scale(1.05);
    text-decoration: underline;
    transition: 0.6s;
}
a.page_accueil
{
    text-decoration: none;
    color:rgba(187, 34, 179,1)!important ;
}
li a.page_veille
{
    color:rgba(187, 34, 179,1)!important ;
    text-decoration: none !important;
}
a.page_bts 
{
    text-decoration: underline;
}
ul.list_header_navbar li.social_liste:hover 
{
    opacity: 0.6;
    transform: scale(1);
}

@media screen and (max-width : 768px){
    .togglebutton 
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
    .bloc_myname 
    {
        display: block;
        position: relative;
        z-index: 30;
    }
    .navbarisopen .open 
    {
        display: block;
    }
    .navbarisopen .close 
    {
        display: none;
    }

    .navbarisopen.yes .open 
    {
        display: none;
    }
    .navbarisopen.yes .close 
    {
        display: block;
    }
    ul.list_header_navbar 
    {
        position: absolute;
        top: 37px;
        left: 0px;
        width: 100%;
        height: 100vh;
        background-color: rgb(187, 34, 179);
        display: flex;
        flex-direction: column;
        justify-content: center;
        transform: translateX(-100%);
        transition: 1s;
        padding-left: 0;
    }
    ul.list_header_navbar li 
    {
        margin-top: 1em;
    }
    .yes ul.list_header_navbar 
    {
        transform: translateX(0%);
    }
}

@media screen and (max-width:570px)
{
    section.introduction_bts_sio 
    {
        padding: 0 3rem;
    }
}
  </style>
  