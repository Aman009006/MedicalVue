<template>
    <transition  name="modal-animation">
        <div v-show="modalActive" v-if="succesModal===false" class="modal">
            <transition  name="modal-animation-inner">
             <div>
                   <div v-show="modalActive"  class="modal-inner">
                <div class="modal_img">
                    <button class="close__btn" type="button" @click="close"><img src="../assets/images/icons/close.svg" alt=""></button>
                    <img src="../assets/images/modal.svg" alt="" class="modal__img">
                </div>

                <div  class="modal__content">
                <div v-if="numberModal === 300" class="first__content">
                    <div  class="container">
                <p class="modal__title">Эта возможность доступна только авторизованным пользователям.</p>
                <p class="modal__descr">Для входа в портал Checkin вам нужно авторизоваться</p>
                <div class="modal-input__content items-center ">
                    <p class="modal-input__title">Введите номер телефона</p>
                    <div class="inputs flex">
                    <p class="number__input">+996</p>
                    <input v-model="numberPhone" type="text" class="modal__input">
                    </div>
                </div>
                    <button @click="sendNumber" class="modal__btn">
                    Далее
                    </button>
                    <div class="modal__navigation">
                    <img src="../assets/images/nav1.svg" alt="" class="nav1">
                    </div>
                </div>
                </div>

                <div v-if="numberModal === 200" class="first__content">
                    <div  class="container">
                <p class="modal__second_title">Код подтверждения.</p>
                <p class="modal__descr-second">На номер телефона <span>+996 {{numberPhone}}</span> выслан код подверждения, введите код чтобы получить доступ к данным пользователя</p>
                    
                   <CodeInput
                   class="input__code"
                        @complete="onComplate"
                        :fields="6"
                        :fieldWidth="50"
                        :fieldHeight="50"
                        :required="true"
                    />
                    <div class="change__number flex  ">
                        <img src="../assets/images/change.svg" alt="" class="change__img">
                        <p class="change__title">Изменить номер телефона</p>
                    </div>
                    <p class="repeat">
                        Повторно отправить код {{ countDown }}
                    </p>

                    <button @click="sendNumber" class="modal__btn">
                    Сохранить
                    </button>
                    <div class="modal__navigation">
                    <img src="../assets/images/2.svg" alt="" class="nav1">
                    </div>
                </div>
                </div>
            </div>

            </div>
            <ReagistrationModal @closeReg="toggleModalReg" :modalRegActive="modalRegActive" ></ReagistrationModal>


             </div>
            </transition>
        </div>
    </transition>
    <!-- <transition name="modal-animation">
        <div v-if="succesModal===true "  @click="()=> { succesModal.value===false; close() }"  class=" modal__success">
            <transition  name="modal-animation-inner" class="">
                <div v-show="modalActive"  class="modal-inner  ">
                    <div class="p-5">
                        <img src="../assets/images/success.svg" alt="" class="success__img">
                    <p class="success__title">
                        Вы успешно <br/> авторизованы
                    </p>
                    </div>
                </div>
            </transition>
        </div>
    </transition> -->
</template>

<script>
import axios from 'axios'
import {ref} from "vue";
import CodeInput from './CodeInput.vue'
import ReagistrationModal from './ReagistrationModal.vue';

 
export default {
 props: ["modalActive"],
 components: { CodeInput, ReagistrationModal },
 setup(props,{emit}){
    const numberModal = ref(300)
    const succesModal = ref(false)
    const numberPhone = ref("")
    const modalRegActive = ref(false);

    const toggleModalReg = () => {
      modalRegActive.value = !modalRegActive.value
    } 


    const close =()=>{
        emit("close")
    }

    const sendNumber = () => {
        const data = new FormData()
        data.append('phone', `${"996" + numberPhone.value}`)
        axios.post('https://api.checkin.kg/api/v2/portal/user/login/password/get', data)
      .then(function (response) {
        numberModal.value = response.status
      })
      .catch(function (error) {
        console.log(`${"996" + numberPhone.value}`);
        alert(error);
      });
    }

    function onComplate(v) {
          const data = new FormData()
        data.append('phone', `${"996" + numberPhone.value}`)
        data.append('code', v)
        axios.post('https://api.checkin.kg/api/v2/portal/user/login/password/set', data)
      .then(function (response) {
        numberModal.value = response.status
        console.log(response.data);
        localStorage.setItem('userToken', response.data.token)
        localStorage.setItem('user_id', response.data.user_id)
        // succesModal.value = true
        toggleModalReg()
        // close()
      })
      .catch(function (error) {
        console.log(`${"996" + numberPhone.value}`,v);
        alert(error);
      });
    }
    return{ close , numberModal ,sendNumber, onComplate,numberPhone,succesModal,modalRegActive,toggleModalReg}
 },
 methods: {
    onChange(v) {
      console.log("onChange ", v);
    },
    onComplete(v) {
      console.log("onComplete ", v);
    }
  }
};
</script>

<style scoped>
body{
    overflow: hidden;
}
.success__title{
    font-weight: 600;
font-size: 24px;
line-height: 32px;
text-align: center;
color: #2B2C3A;
margin-top: 16px;
width: 342px;
height: 64px;
}
.modal__success{
    margin:0 auto !important;
    display: flex !important;
    align-items: center;
    justify-content: center;
    position: fixed;
    background: rgba(43, 44, 58, 0.15);
    backdrop-filter: blur(5px);
    height: 100vh;
    width: 100%;
    z-index: 999;
        
}
.success__img{
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
}
.input__code{
    margin-bottom: 32px;
}
.modal__second_title{
    font-weight: 700;
font-size: 24px;
line-height: 29px;
/* identical to box height */

text-align: center;
letter-spacing: 0.15px;
text-transform: uppercase;

color: #6197FF;
margin-bottom: 10px;
}
.modal__descr-second{
    font-weight: 400;
font-size: 14px;
line-height: 150.02%;

text-align: center;
letter-spacing: 0.01em;

color: rgba(43, 44, 58, 0.8);
margin-bottom: 32px;
}
.change__number{
    margin-bottom: 40px;
    display: flex;
    align-items: center;
    justify-content: center;
}
.change__title{
    font-weight: 400;
font-size: 14px;
line-height: 16px;
display: flex;
align-items: center;
text-align: center;
letter-spacing: 1px;
margin-left: 8px;
color: #6197FF;
}
.modal{
    position: fixed;
    background: rgba(43, 44, 58, 0.15);
    backdrop-filter: blur(5px);
    height: 100vh;
    width: 100%;
    z-index: 999;
}
.repeat{
    margin-bottom: 48px;
    font-weight: 400;
font-size: 14px;
line-height: 16px;
text-align: center;
letter-spacing: 1px;
color: rgba(43, 44, 58, 0.5);
width: 100%;
}
.modal-inner{
    margin: 34px auto;
    background: white;
    width: 374px;
    border-radius: 8px;
}
.modal_img{
    background: #EAF3FB;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    width: 374px;
    height: 244px;
    border-top-left-radius: 8px;
    border-top-right-radius: 8px;

}
.modal__content{
    padding: 16px;
}
.modal__title{
    font-weight: 600;
font-size: 18px;
line-height: 130%;
display: flex;
align-items: center;
text-align: center;
letter-spacing: 0.5px;

color: #6197FF;
margin-bottom: 10px;
}
.modal__descr{
    font-weight: 400;
font-size: 14px;
line-height: 20px;
/* or 143% */

display: flex;
align-items: center;
text-align: center;

color: rgba(43, 44, 58, 0.6);
margin-bottom: 38px;
}
.modal-input__content{
width: 342px;
background: #EAF3FB;
border: 1px solid #CBE7FF;
border-radius: 8px;
padding: 9px 16px;
}
.modal-input__title{
    font-weight: 400;
font-size: 10px;
line-height: 12px;
letter-spacing: 0.01em;

color: rgba(43, 44, 58, 0.5);
margin-bottom: 2px;
}
.modal__input{
    background: none;
    margin-left: 4px;
}
.number__input{
    font-weight: 500;
font-size: 16px;
line-height: 24px;
/* identical to box height, or 150% */

letter-spacing: 0.01em;

color: #2B2C3A;
}
.modal-input__content{
    margin-bottom: 130px;
}
.modal__btn{
    width: 342px;
height: 56px;
background: #6197FF;
border-radius: 31px;
display: flex;
align-items: center;
justify-content: center;
font-weight: 500;
font-size: 16px;
line-height: 19px;
display: flex;
align-items: center;
text-align: center;
letter-spacing: 0.5px;
color: #FFFFFF;
margin-bottom: 32px;
}
.modal__navigation{
    margin-bottom: 32px;
    display: flex;
    align-items: center;
    justify-content: center;
}
.close__btn{
    position: absolute;
    top: 16px;
    right: 16px;
}
</style>