<template>
    <header class="Header">
        <nav class="Header-navbar" :class="displayNav ? 'yes' : ''">
          <div>
            <h1 class="Header-title">BEAUTY MS</h1>
          </div>
          <div class="Header-toggleButton" @click="displaynav">
            <span class="bar1"></span>
            <span class="bar2"></span>
            <span class="bar3"></span>
          </div>
          <ul class="Header-blocNavigation">  
            <li><router-link to="/accueil">Accueil</router-link></li>
            <li><router-link to="/about">Contact</router-link></li>
            <li class="Header-instagramButton"> <a href="https://www.instagram.com/beauty.ms_95/?hl=fr" target="_blank"><img src="../../assets/instagram1.png"  alt="Logo instagram"/></a></li>
            <li class="Header-snapchatButton"> <a href="" target="_blank"><img src="../../assets/snapchat.png"  alt="Logo snapchat"/></a></li>
          </ul>
        </nav>
      </header>
  </template>
  
  <script>


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
    }
};
  </script>
  <style scoped>

.Header 
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

.Header-title
{
    font-size: 2.5em;
    background-color: rgba(187, 34, 179,0);
    text-decoration: overline;
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
        height: 72vh;
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
  </style>
  