<template>
   <nav>
    <div class="container">
     <div class="nav__links">
        <router-link to="/"><img class="def__svg" src="./assets/images/icons/home1.svg" alt=""> <img class="active__svg" src="./assets/images/icons/active1.svg" alt=""> <span class="nav__span">Главная</span></router-link> 
      <router-link to="/medcard"><img class="def__svg" src="./assets/images/icons/home2.svg" alt=""><img class="active__svg" src="./assets/images/icons/active2.svg" alt=""><span class="nav__span">Медицинская карта</span></router-link>  
      <router-link to="/track"><img class="opacity def__svg" src="./assets/images/icons/home3.svg" alt=""><img class="active__svg" src="./assets/images/icons/active3.svg" alt=""><span class="nav__span">Трекер здоровья</span></router-link> 
      <router-link to="/profile"><img class="def__svg" src="./assets/images/icons/home4.svg" alt=""><img  class="active__svg" src="./assets/images/icons/active4.svg" alt=""><span class="nav__span">Профиль</span></router-link>
     </div>
    </div>
  </nav>
  <router-view />
</template>

<script>

export default {
  components: {
  },
}
</script>

<style>
nav {
height: 56px;
position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  background: white;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 99;
}
.opacity{
  opacity: 0.5;
}
.nav__links{
  display: flex;
  align-items: center;
  justify-content: space-between;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  display: flex;
}
nav a active__svg{
  display: none;
}

nav a span{
  display: none;
}
nav a.router-link-exact-active {
  color: white;
  display: flex;
  background: #6197FF;
border-radius: 50px;
animation: animatename 0.1s  ;
  padding: 10px;
}
nav a.router-link-exact-active img.def__svg {
  display: none;
}
nav a.router-link-exact-active span {
display: block;
/* animation: animatename 0.5s  ; */
}
@keyframes animatename{
  0%{
   padding: 0;
  }
 
  100%{
  padding: 10px;
  }
}

nav a.router-link-exact-active img {
 margin-right: 12px;
}

@import url('https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800;900&display=swap');
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Inter', sans-serif;
}

.container{
  max-width: 374px;
  width: 100%;
  margin: 0 auto;
}
.bg__white{
  background-color: white !important;
}
.login{
  background: none;
  border: none;
}
@media only screen and (max-width: 400px) {
  .container{
    padding: 0 15px;
  }
}
</style>
