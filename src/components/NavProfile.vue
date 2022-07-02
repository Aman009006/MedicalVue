<template>
  <div class="profile">
    <div class="container">
      <div class="profile__content">
        <div class="profile__title">Мой профиль</div>
        <img src="../assets/images/icons/logout.svg" alt="" class="profile__img">
      </div>
    </div>
  </div>
</template>

<script>
  export default {
  name: 'NavProfile',
  props: {
    msg: String
  }
}
</script>

<style >

.profile{
  padding: 16px;
  background: white;
}
.profile__content{
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.profile__title{
  font-weight: 500;
font-size: 18px;
line-height: 24px;
display: flex;
align-items: center;
letter-spacing: 0.15px;
color: #2B2C3A;
}

</style>
