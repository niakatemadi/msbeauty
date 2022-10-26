<template>
  <footer class="Footer">
    <h1 class="Footer-title">Nos coordonnées </h1>
    <section>
      <div><img src="../../assets/emplacement.png"  alt="icone localisation"/> <p>85 Route d'Eragny à Bessancourt</p><p>95220 Pierrelaye</p></div>
      <div><img src="../../assets/telephone-portable.png"  alt="icone telephone"/> <p>Appelez-nous au :</p><p>07 66 22 04 25</p></div>
      <div><img src="../../assets/email.png"  alt="icone email"/><p>Contactez-nous par email :</p><p>xxxx@gmail.com</p></div>
    </section>
  </footer>
</template>

<style scoped>
.Footer{
  width:100%;
  margin-top:100px;
  color: rgba(187,34,179);
  background: rgb(192, 192, 192);
  background: linear-gradient(180deg,rgb(192, 192, 192)  0%, rgba(33, 28, 33, 0.889) 90%);
  text-align:center;
  font-family: 'Playfair Display', serif;
}
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