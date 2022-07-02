<template>
    <transition v-show="modalRegActive" name="modal-registation">
        <div class="registation__modal">
            <div class="container">
                <div class="reg__content">
                    <p class="reg__title">Для полного пользования нашим сервисом, пройдите регистрацию.</p>
                    <div class="reg__descr">(*обязательные поля)</div>
                    <div class="inputs">
                        <input type="text" class="reg__input" v-model="fullName"  placeholder="Введите ФИО*">
                    <input v-model="DOB" type="date"
                        min="1950-01-01"  class="reg__input" max="2032-02-20" placeholder="Введите дату рождения*">
                    </div>

                    <div class="buttons">
                        <button :class="{ active__btn: succesModal }" @click="succesModal = !succesModal" class="sex__btn ">Мужчина</button>
                        <button :class="{ active__btn: !succesModal }" @click="succesModal = !succesModal" class="sex__btn ">Женщина</button>
                    </div>

                    <div class="btn__success">
                        <button @click="upDateProfile" class="btnsucces">Далее</button>
                    </div>
                    <img src="../assets/images/step1.svg" alt="" class="step1">
                    </div>
                </div>
            </div>
    </transition>
</template>

<script>
import {ref} from "vue";
import axios from 'axios'


export default {
  props: ["modalRegActive"],


setup(props,{emit}){
    const succesModal = ref(false)
    const userToken = localStorage.getItem('userToken')
    const fullName = ref("")
    const DOB = ref()

   

    const upDateProfile = () => {
        const regData = new FormData()
        regData.append('full_name', fullName.value )
        regData.append('sex', `${succesModal.value ? "male" : "female"}` )
        regData.append('DOB', DOB.value.replace(/-/g,".").split('.').reverse().join().replace(/,/g,".") )
        axios.post('https://api.checkin.kg/api/v2/portal/user/update', 
         regData ,{ headers: {"Authorization" : `Token ${userToken}`} })

      .then(function () {
        close()
        closeReg()
      })
      .catch(function (error) {
        alert(error);
        console.log(regData);
      });
    }
    
    const closeReg =()=>{
        emit("closeReg")
    }
    return{closeReg,succesModal,upDateProfile,userToken,fullName,DOB}
}
}
</script>

<style >
.buttons{
background: #FFFFFF;
border: 1.5px solid #F4F4F9;
border-radius: 8px;
display: flex;
align-items: center;
justify-content: space-between;
padding: 5px;
margin-bottom: 160px;
}
.step1{
    margin: 0 auto;
}
.btn__success{
    margin-bottom: 42px;
}
.btnsucces{
    width: 374px;
height: 56px;
display: flex;
align-items: center;
justify-content: center;
background: #6197FF;
border-radius: 50px;
color: white;
font-weight: 500;
font-size: 14px;
line-height: 17px;
letter-spacing: 0.75px;
text-transform: uppercase;
color: #FFFFFF;
}
.sex__btn{
       width: 179.5px;
height: 48px;
}
.active__btn{
    width: 179.5px;
height: 48px;

background: #6197FF;
box-shadow: 1px 2px 3px -2px rgba(24, 39, 75, 0.1);
border-radius: 4px;
color: white;
}
.registation__modal{
    z-index: 9999;
    position: fixed;
    top: 0;
}
.reg__input{
    width: 374px;
height: 56px;
padding: 16px;
background: #F4F4F9;
border-radius: 8px;
margin-bottom: 24px;
}
.inputs{
    display: block;
}
.reg__descr{
    font-weight: 400;
font-size: 16px;
line-height: 24px;
letter-spacing: 0.01em;
color: rgba(43, 44, 58, 0.6);
margin-bottom: 32px;
}
.reg__title{
    font-weight: 600;
font-size: 24px;
line-height: 32px;
padding-top: 90px;
color: #6197FF;
margin-bottom: 8px;
}

.registation__modal{
    background: white;
    height: 100vh;
    width: 100%;
}
</style>
