<template>
<div class="controller__content">
    <div class="container">
        <div class="controll__btn">
            <div class="controll__icon">
                <img src="../assets/images/icons/icon-type.svg" alt="" class="icon">                
            </div>
            <div class="controll__text">
                <p class="controll__title">Записи</p>
                <p class="controll__descr">Следите за здоровьем своего ребенка</p>
            </div>
        </div>
        <div class="controll__btn">
            <div class="controll__icon">
                <img src="../assets/images/icons/icon-family.svg" alt="" class="icon">                
            </div>
            <div class="controll__text">
                <p class="controll__title">Записи</p>
                <p class="controll__descr">Следите за здоровьем своего ребенка</p>
            </div>
        </div>
        <div class="controll__btn">
            <div class="controll__icon">
                <img src="../assets/images/icons/icon-sale.svg" alt="" class="icon">                
            </div>
            <div class="controll__text">
                <p class="controll__title">Записи</p>
                <p class="controll__descr">Следите за здоровьем своего ребенка</p>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
  name: 'NavController',
  props: {
    msg: String
  }
}
</script>

<style >
.controller__content{
    margin-top: 16px;

}
.controll__btn{
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    max-width: 374px;
    width: 100%;
    height: 70px;
    background: #FFFFFF;
box-shadow: 0px 2px 4px -2px rgba(24, 39, 75, 0.12), 0px 4px 4px -2px rgba(24, 39, 75, 0.08);
border-radius: 8px;
padding: 12px;
margin-bottom: 12px;
cursor: pointer;
}
.controll__icon{
    width: 44px;
height: 44px;
background: rgba(238, 238, 238, 0.5);
border-radius: 8px;
display: flex;
align-items: center;
justify-content: center;
}
.controll__text{
    width: 294px;
}
.controll__title{
    font-weight: 400;
font-size: 16px;
line-height: 24px;
letter-spacing: 0.01em;
color: #2B2C3A;
}
.controll__descr{
    font-weight: 400;
font-size: 14px;
line-height: 20px;
letter-spacing: 0.1px;
color: rgba(43, 44, 58, 0.5);
}
</style>
