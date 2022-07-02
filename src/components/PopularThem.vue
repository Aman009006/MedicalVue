<template>
<div class="theme__content">
    <div class="container theme__container">
        <p class="popular__title">Популярные темы</p>
        <swiper
        class="slider__popular"
    :modules="modules"
    :slides-per-view="4"
    :space-between="65"
    :pagination="{ clickable: true }"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
  >
    <swiper-slide class="swiper__slider"><img src="../assets/images/slider-img1.png" alt="" class="swiper__img"> <p class="swiper__text">Акция - кешбек временно...</p></swiper-slide>
    <swiper-slide class="swiper__slider"><img src="../assets/images/slider-img2.png" alt="" class="swiper__img"> <p class="swiper__text">Хотим узнать ваше мнение</p></swiper-slide>
    <swiper-slide class="swiper__slider"><img src="../assets/images/slider-img3.png" alt="" class="swiper__img"> <p class="swiper__text">Дарите близким здоровье</p></swiper-slide>
    <swiper-slide class="swiper__slider"><img src="../assets/images/slider-img4.png" alt="" class="swiper__img"> <p class="swiper__text">Хотим узнать ваше мнение</p></swiper-slide>
    <swiper-slide class="swiper__slider"><img src="../assets/images/slider-img2.png" alt="" class="swiper__img"> <p class="swiper__text">Акция - кешбек временно...</p></swiper-slide>
    <swiper-slide class="swiper__slider"><img src="../assets/images/slider-img3.png" alt="" class="swiper__img"> <p class="swiper__text">Акция - кешбек временно...</p></swiper-slide>
    <swiper-slide class="swiper__slider"><img src="../assets/images/slider-img4.png" alt="" class="swiper__img"> <p class="swiper__text">Акция - кешбек временно...</p></swiper-slide>
    <swiper-slide class="swiper__slider"><img src="../assets/images/slider-img2.png" alt="" class="swiper__img"> <p class="swiper__text">Акция - кешбек временно...</p></swiper-slide>
    <swiper-slide class="swiper__slider"><img src="../assets/images/slider-img3.png" alt="" class="swiper__img"> <p class="swiper__text">Акция - кешбек временно...</p></swiper-slide>
    <swiper-slide class="swiper__slider"><img src="../assets/images/slider-img4.png" alt="" class="swiper__img"> <p class="swiper__text">Акция - кешбек временно...</p></swiper-slide>
  </swiper>
    </div>
</div>
</template>

<script>
    import { Swiper, SwiperSlide } from 'swiper/vue';
    import { Navigation, Pagination, Scrollbar, A11y } from 'swiper';
     import 'swiper/css';
  import 'swiper/css/navigation';
  import 'swiper/css/pagination';
  import 'swiper/css/scrollbar';
export default {
  name: 'PopularThem',
  props: {
    msg: String
  },
  components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
         modules: [Navigation, Pagination, Scrollbar, A11y],
      };
    },
}
</script>

<style >

.theme__content{
    margin-top: 24px;

}
.swiper-horizontal>.swiper-pagination-bullets, .swiper-pagination-bullets.swiper-pagination-horizontal, .swiper-pagination-custom, .swiper-pagination-fraction{
    position: absolute !important;
    top: 0px !important;
    right: 0px !important;
    left: 60% !important;
}
.swiper-pagination-bullet{
    width: 8px;
height: 8px;
background: #FFFFFF !important;
opacity: 1 !important;
}
.swiper-pagination-bullet-active{
    width: 12.8px;
height: 8px;

background: #6197FF !important;
border-radius: 5px;
}
.swiper-pagination-fraction{
    left: 1 !important;
}
.swiper{
    position: initial !important;
}
.swiper__img{
  max-width: 181px !important;
  /* width: 100%; */
}
.theme__container{
    position: relative;
        padding-bottom: 12px !important;
    border-bottom: 1px solid rgba(43, 44, 58, 0.1);
}
.swiper-pagination{
    position: absolute !important;
    top: 0 !important;
    right: 0 !important;
    height: 8px;
    max-width: 150px;
    width: 100%;
}
.popular__title{
font-weight: 600;
font-size: 20px;
line-height: 28px;
letter-spacing: 0.15px;
color: #2B2C3A;
margin-bottom: 12px;
}
/* .swiper__slider{
    position: relative;
    width: 100px;
    height: 100px;
} */
.swiper__text{
   margin: auto;
  position: absolute;
  left: 8px; bottom: 8px; right: 8px;
    font-weight: 400;
font-size: 9px;
line-height: 11px;
letter-spacing: 0.1px;
color: #FFFFFF;
width: 84px;
height: 22px;
}
</style>
