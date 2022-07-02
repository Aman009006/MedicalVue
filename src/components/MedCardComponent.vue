<template>
 <div class="bg__white mt1">
   <div class="container">
    <div class="health__content">
          <div class="news__titls medcard__title">
          <p class="news__titles">Медицинская карта</p>
          <a href="#" class="arrow"> <img src="../assets/images/icons/arrow2.svg" alt=""></a>
        </div>
    </div>
    <div class="health__data">
        <div class="health__indicate">
            <div class="indicate">
                <div class="data__indicate">
                <img src="../assets/images/icons/indicate1.svg" alt="" class="indicate__img">
                <div class="indicate__title">Кровь</div>
            </div>
            <div class="indicate__answer">А+</div>
            </div>
            <div class="indicate">
                <div class="data__indicate">
                <img src="../assets/images/icons/indicate2.svg" alt="" class="indicate__img">
                <div class="indicate__title">Вес</div>
            </div>
            <div class="indicate__answer">65</div>
            </div>
            <div class="indicate">
                <div class="data__indicate">
                <img src="../assets/images/icons/indicate3.svg" alt="" class="indicate__img">
                <div class="indicate__title">Рост</div>
            </div>
            <div class="indicate__answer">170</div>
            </div>
        </div>
        <div class="health__ilnes">
            <div class="health__allergy">
                <p class="allergy__title">Аллергия</p>
                <p class="allergy__count">3</p>
            </div>
             <div class="health__allergy">
                <p class="ill__title">Хронические заболевания</p>
                <p class="allergy__count">5</p>
            </div>
        </div>
    </div>
  </div>
 </div>
</template>

<script>
export default {
  name: 'NavigationCont',
  props: {
    msg: String
  }
}
</script>

<style >
.health__data{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.allergy__count{
    font-weight: 700;
font-size: 16px;
line-height: 24px;
letter-spacing: 0.01em;
color: #2B2C3A;
}
.indicate__answer{
    font-weight: 700;
font-size: 16px;
line-height: 24px;
letter-spacing: 0.01em;
color: #2B2C3A;
}
.indicate__title{
    font-weight: 500;
font-size: 14px;
line-height: 20px;
display: flex;
align-items: center;
letter-spacing: 0.005em;
color: rgba(43, 44, 58, 0.5);
}
.allergy__title{
    font-weight: 500;
font-size: 14px;
line-height: 20px;
display: flex;
align-items: center;
letter-spacing: 0.005em;
color: #6197FF;
height: 30px;

}
.health__allergy{
    margin-bottom: 12px;
}
.health__allergy:last-child{
    margin-bottom: 0;
}
.ill__title{
    font-weight: 500;
font-size: 14px;
line-height: 20px;
display: flex;
align-items: center;
letter-spacing: 0.005em;
color: #FF6197;
height: 30px;
}
.medcard__title{
    padding-top: 16px;
    padding-bottom: 16px;
}
.health__allergy{
    background: #FFFFFF;
border: 1px solid rgba(244, 244, 249, 0.5);
box-shadow: 0px 2px 4px -2px rgba(24, 39, 75, 0.12), 0px 4px 4px -2px rgba(24, 39, 75, 0.08);
border-radius: 8px;
display: flex;
align-items: center;
justify-content: space-between;
padding: 16px;
width: 180px;
}
.health__indicate{
background: #FFFFFF;
border: 1px solid rgba(244, 244, 249, 0.5);
box-shadow: 0px 2px 4px -2px rgba(24, 39, 75, 0.12), 0px 4px 4px -2px rgba(24, 39, 75, 0.08);
border-radius: 8px;
max-width: 181px;
width: 100%;
padding: 16px;
margin-right: 12px;
}
.health__data{
    padding-bottom: 16px;
}
.indicate{
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 20px;
}
.indicate:last-child{
    margin-bottom: 0px;
}
.data__indicate{
    max-width: 75px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

</style>
