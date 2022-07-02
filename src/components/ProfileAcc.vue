<template>
  <div class="profile__acc">
    <div class="container">
      <div class="profileacc__content">
        <img src="../assets/images/icons/profile__img.svg" alt="" class="profile__img">
        <div class="profile__text">
            <p class="profile__name">Активные сеансы</p>
            <p class="profile__number">3 девайса</p>
        </div>
        <img src="../assets/images/icons/edit_p.svg" alt="" class="edit__img">
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
.profileacc__content{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.profile__acc{
    padding: 16px;
    background: white;
}
.profile__text{
    max-width: 274px;
    width: 100%;
}
.profile__name{
    font-weight: 600;
font-size: 16px;
line-height: 24px;
display: flex;
align-items: center;
letter-spacing: 0.01em;
color: #2B2C3A;
}
.profile__number{
    font-weight: 400;
font-size: 14px;
line-height: 20px;
letter-spacing: 0.005em;
color: rgba(43, 44, 58, 0.5);
}
</style>
