<template>
  <div class="aboutapp">
    <div class="container">
        <div class="aboutapp__content">
           <p class="aboutapp__title">Информация о приложении</p>
           <div class="feedback">
            <img src="../assets/images/icons/sms.svg" alt="" class="feedback__img">
            <p class="feedback__title">Оставить отзыв</p>
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
.aboutapp__title{
    font-weight: 700;
    font-size: 16px;
    line-height: 24px;
    letter-spacing: 0.01em;
    color: #6197FF;
}
.feedback__title{
    margin-left: 18px;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    letter-spacing: 0.01em;
    color: #2B2C3A;
}
.feedback{
    display: flex;
    align-items: center;
    justify-content: start;
    margin-top: 32px;
}
.aboutapp{
    padding: 16px;
    background: white;
    margin-bottom: 58px;
}
</style>
