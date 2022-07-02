<template>
  <div class="seanse">
    <div class="container">
        <div class="seanse__container">
            <img src="../assets/images/icons/active__svg.svg" alt="" class="seanse__img">
            <div class="profile__text">
                <p class="profile__name">Мамыров Максат</p>
                <p class="profile__number">+996 505 44 55 34</p>
            </div>
            <img src="../assets/images/icons/arrow3.svg" alt="" class="arrow3">
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
.seanse{
    margin-top: 16px;
    background: white;
}
.seanse__container{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.seanse__container{
    padding: 16px 4px;
}
</style>
