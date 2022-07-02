<template>
 <div class="health__categories">
    <div class="container">
        <div class="health__categories_content">
            <div class="health__category">
                <img src="../assets/images/icons/ct1.svg" alt="" class="heath__category_img">
                <p class="health__category_title">Приёмы</p>
            </div>
            <div class="health__category">
                <img src="../assets/images/icons/ct2.svg" alt="" class="heath__category_img">
                <p class="health__category_title">Приёмы</p>
            </div>
            <div class="health__category">
                <img src="../assets/images/icons/ct3.svg" alt="" class="heath__category_img">
                <p class="health__category_title">Приёмы</p>
            </div>
            <div class="health__category">
                <img src="../assets/images/icons/ct4.svg" alt="" class="heath__category_img">
                <p class="health__category_title">Приёмы</p>
            </div>
            <div class="health__category">
                <img src="../assets/images/icons/ct5.svg" alt="" class="heath__category_img">
                <p class="health__category_title">Приёмы</p>
            </div>
            <div class="health__category">
                <img src="../assets/images/icons/ct6.svg" alt="" class="heath__category_img">
                <p class="health__category_title">Приёмы</p>
            </div>
            <div class="health__category">
                <img src="../assets/images/icons/ct7.svg" alt="" class="heath__category_img">
                <p class="health__category_title">Приёмы</p>
            </div>
            <div class="health__category">
                <img src="../assets/images/icons/ct8.svg" alt="" class="heath__category_img">
                <p class="health__category_title">Приёмы</p>
            </div>
        </div>
    </div>
 </div>
</template>

<script>
export default {
  name: 'HealthCategory',
  props: {
    msg: String
  }
}
</script>

<style >
.health__categories_content{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 70px;
}
.health__categories{
    margin-top: 16px;
}
.health__category{
background: #FFFFFF;
box-shadow: 0px 2px 4px -2px rgba(24, 39, 75, 0.12), 0px 4px 4px -2px rgba(24, 39, 75, 0.08);
border-radius: 8px;
padding: 12px;
width: 180px;
margin-bottom: 12px;
}
.health__category_title{
    margin-top: 12px;
    text-align: center;
}
.heath__category_img{
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
}
</style>
