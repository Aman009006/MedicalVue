<template>
 <div class="bg__white mt1">
   <div class="btn__search">
      <div class="container">
        <button class="nav__btn">
        <img class="btn__img" src="../assets/images/btn__img.svg" alt=""> <span>Найти врача или организацию</span>
      </button>
      </div>
    </div>
 </div>
</template>

<script>
export default {
  name: 'MainNav',
  props: {
    msg: String
  }
}
</script>

<style >
.mt1{
  margin-top: 1px;
}
.navigation__content{
  height: 70px;
  display: flex;
  align-items: center;
  justify-content: flex-end;
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
  /* border-top: 2px solid #E5E5E5; */
  padding: 16px 0px;
}
</style>
