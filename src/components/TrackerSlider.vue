<template>
<div class="theme__content">
    <div class="container tracking__slider">
        <p class="popular__title">Популярные темы</p>
        <swiper
        class="slider__popular"
    :modules="modules"
    :slides-per-view="1"
    :space-between="10"
    :pagination="{ clickable: true }"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
  >
    <swiper-slide ><img src="../assets/images/icons/track__banner.png" alt="" class="swiper__img"></swiper-slide>
    <swiper-slide ><img src="../assets/images/icons/track__banner.png" alt="" class="swiper__img"></swiper-slide>
    <swiper-slide ><img src="../assets/images/icons/track__banner.png" alt="" class="swiper__img"></swiper-slide>
    <swiper-slide ><img src="../assets/images/icons/track__banner.png" alt="" class="swiper__img"></swiper-slide>
    <swiper-slide ><img src="../assets/images/icons/track__banner.png" alt="" class="swiper__img"></swiper-slide>
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

<style scoped>
.swiper__img {
    width: 365px !important;
}
.theme__content{
    margin-top: 24px;
}
.swiper-slide{
    width: 378px !important;
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
.tracking__slider{
    position: relative;
        padding-bottom: 12px !important;
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
