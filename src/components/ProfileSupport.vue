<template>
  <div class="support">
    <div class="container">
        <div class="support__content">
            <img src="../assets/images/icons/support.svg" alt="" class="logo__support">
            <p class="support__title">Cлужба поддержки</p>
            <p class="support__descr">У вас возникли сложности с пользованием  checkin, свяжитесь с нами!</p>
            <button class="support__btn">связаться</button>
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
.logo__support{
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
}
.support{
    background: white;
    padding: 16px;
    margin-top: 16px;
    margin-bottom: 16px;
}
.support__title{
    margin-top: 12px;
    font-weight: 600;
    font-size: 18px;
    line-height: 22px;
    text-align: center;
    letter-spacing: 0.15px;
    color: #2B2C3A;
}
.support__descr{
    margin-top: 8px;
    font-weight: 400;
    font-size: 14px;
    line-height: 17px;
    text-align: center;
    letter-spacing: 0.15px;
    color: rgba(43, 44, 58, 0.5);
    max-width: 374px;
    width: 100%;
}
.support__btn{
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
    margin-top: 16px;
    background: #6197FF;
    box-shadow: 0px 2px 4px -2px rgba(24, 39, 75, 0.12), 0px 4px 4px -2px rgba(24, 39, 75, 0.08);
    border-radius: 40px;
    font-weight: 500;
    font-size: 14px;
    line-height: 17px;
    letter-spacing: 0.75px;
    text-transform: uppercase;
    color: #FFFFFF;
    height: 48px;
    max-width: 232px;
    width: 100%;
    border: none;
}
</style>
