<template>
<div class="category__content">
    <div class="container">
      <div class="category__carts">
        <div class="category__cart">
          <p class="category__cart_title">Детский врач</p>
          <img src="../assets/images/category1.png" alt="" class="category__cart_img">
        </div>
        <div class="category__cart">
          <p class="category__cart_title">Голованая боль</p>
          <img src="../assets/images/category2.png" alt="" class="category__cart_img">
        </div>
        <div class="category__cart">
          <p class="category__cart_title">Проблемы c зубами</p>
          <img src="../assets/images/category3.png" alt="" class="category__cart_img">
        </div>
        <div class="category__cart">
          <p class="category__cart_title">Боль в спине</p>
          <img src="../assets/images/category4.png" alt="" class="category__cart_img">
        </div>
      </div>
      <button class="category__btn">
        Посмотреть все
      </button>
    </div>
</div>
</template>

<script>
export default {
  name: 'CategoryContent',
  props: {
    msg: String
  }
}
</script>

<style >
.category__content{
  margin-top: 12px;
}
.category__carts{
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  justify-content: space-between;
}
.category__cart{
max-width: 170px;
width: 100%;
height: 76px;
background: #FFFFFF;
border-radius: 8px;
display: flex;
align-items: center;
justify-content: space-between;
padding: 12px;
margin-bottom: 12px;
}
.category__cart_title{
  width: 93px;
}
.category__btn{
max-width: 374px;
width: 100%;
height: 46px;
background: #FFFFFF;
border-radius: 8px;
font-weight: 400;
font-size: 14px;
line-height: 20px;
text-align: center;
letter-spacing: 0.005em;
color: #6197FF;
border: none;
}
</style>
