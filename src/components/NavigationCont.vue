<template>
 <ModalAuth @close="toggleModal" :modalActive="modalActive"> </ModalAuth>
 <div class="bg__white">
   <div class="container">
    <div class="navigation__content">
      <button @click="toggleModal" class="login"><img src="../assets/images/icons/login.svg" alt=""></button>
      <img @click="toggleModalReg" src="../assets/images/notification.svg" class="notification" alt="">
    </div>
  </div>
 </div>
</template>

<script>
import ModalAuth from './ModalAuth.vue';
import {ref} from "vue";

export default {
    components: { ModalAuth },
    
  setup(){
   const modalActive = ref(false);


    const toggleModal = () => {
      modalActive.value = !modalActive.value
    } 
  
   return{modalActive,toggleModal,}
  }
}
</script>

<style scoped >

.navigation__content{
  height: 70px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav__btn{
  display: flex;
  align-items: center;
  justify-content: center;
  background: #6197FF;
box-shadow: 0px 2px 4px -2px rgba(24, 39, 75, 0.12), 0px 4px 4px -2px rgba(24, 39, 75, 0.08);
border-radius: 8px;
padding: 14px 49px;
border: none;
color: white;
max-width: 374px;
width: 100%;
height: 52px;
font-weight: 400;
font-size: 16px;
line-height: 24px;
letter-spacing: 0.01em;
color: #FFFFFF;
margin: 0 auto;
}
.btn__img{
  margin-right: 8px;
}
.btn__search{
  border-top: 2px solid #E5E5E5;
  padding: 16px 0px;
}
</style>
