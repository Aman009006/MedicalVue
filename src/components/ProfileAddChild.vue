<template>
  <div class="child">
    <div class="container">
        <div class="child__content">
            <p class="child__title">Дети</p>
            <div class="input__content">
                <input type="text" placeholder="Нет провиля ваших детей" class="child__input">
                <button class="child__btn"><img src="../assets/images/icons/addch.svg" alt=""> <span>Добавить</span></button>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
  export default {
  props: {
    msg: String
  }
}
</script>

<style >
.child{
    padding: 16px;
    background: white;
    margin-top: 16px;
}
.child__title{
    font-weight: 700;
    font-size: 16px;
    line-height: 24px;
    letter-spacing: 0.01em;
    color: #6197FF;
    margin-bottom: 16px;
}
.input__content{
    display: flex;
    align-items: center;
    justify-content: space-between;
    max-width: 374px;
    width: 100%;
    padding: 14px 12px;
    background: #FFFFFF;
    border: 1px solid rgba(43, 44, 58, 0.1);
    border-radius: 8px;
}
.child__input{
    background: none;
    border: none;
    padding: 2px;
    font-weight: 400;
    font-size: 14px;
    line-height: 17px;
    letter-spacing: 0.15px;
    color: rgba(43, 44, 58, 0.5);
}
.child__btn{
    background: none;
    border: none;
    max-width: 106px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    letter-spacing: 0.01em;
    color: #6197FF;
}
</style>
