<template>
  <div class="track__type__content">
    <div class="container">
        <div class="types">
            <div class="left">
                <div class="tracking__type">
                <img src="../assets/images/icons/types1.svg" alt="" class="type__img">
                <p class="type__title">Онкологический</p>
                <p class="type__descr">Равным образом реализация намеченных плановых заданий позволяет оценить</p>
                <button class="type__add__btn">+ Добавить</button>
            </div>
            <div class="tracking__type">
                <img src="../assets/images/icons/type2.svg" alt="" class="type__img">
                <p class="type__title">Гормональный</p>
                <p class="type__descr">Равным образом реализация намеченных плановых заданий способствует подготовки и реализации позиций, занимаемых участниками </p>
                <button class="type__add__btn">+ Добавить</button>
            </div>
            <div class="tracking__type">
                <img src="../assets/images/icons/types1.svg" alt="" class="type__img">
                <p class="type__title">Онкологический</p>
                <p class="type__descr">Равным образом реализация намеченных плановых заданий позволяет оценить</p>
                <button class="type__add__btn">+ Добавить</button>
            </div>
            <div class="tracking__type">
                <img src="../assets/images/icons/types1.svg" alt="" class="type__img">
                <p class="type__title">Онкологический</p>
                <p class="type__descr">Равным образом реализация намеченных плановых заданий позволяет оценить</p>
                <button class="type__add__btn">+ Добавить</button>
            </div>
            </div>
             <div class="">
            <div class="tracking__type">
                <img src="../assets/images/icons/type2.svg" alt="" class="type__img">
                <p class="type__title">Гормональный</p>
                <p class="type__descr">Равным образом реализация намеченных плановых заданий способствует подготовки и реализации позиций, занимаемых участниками </p>
                <button class="type__add__btn">+ Добавить</button>
            </div>
            <div class="tracking__type">
                <img src="../assets/images/icons/types1.svg" alt="" class="type__img">
                <p class="type__title">Онкологический</p>
                <p class="type__descr">Равным образом реализация намеченных плановых заданий позволяет оценить</p>
                <button class="type__add__btn">+ Добавить</button>
            </div>
            <div class="tracking__type">
                <img src="../assets/images/icons/type2.svg" alt="" class="type__img">
                <p class="type__title">Гормональный</p>
                <p class="type__descr">Равным образом реализация намеченных плановых заданий способствует подготовки и реализации позиций, занимаемых участниками </p>
                <button class="type__add__btn">+ Добавить</button>
            </div>
            <div class="tracking__type">
                <img src="../assets/images/icons/types1.svg" alt="" class="type__img">
                <p class="type__title">Онкологический</p>
                <p class="type__descr">Равным образом реализация намеченных плановых заданий позволяет оценить</p>
                <button class="type__add__btn">+ Добавить</button>
            </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>


export default {
  name: 'TrackingTypes',
  components: {

}
}
</script>

<style>
.types{
   display: flex;
    justify-content: space-between;
}

.track__type__content{
    margin-bottom: 100px;
}
.left{
    margin-right: 12px;
}
.tracking__type{
    max-width: 181px;
    width: 100%;
background: #FFFFFF;
box-shadow: 0px 2px 4px -2px rgba(24, 39, 75, 0.12), 0px 4px 4px -2px rgba(24, 39, 75, 0.08);
border-radius: 8px;
padding: 12px;
margin-bottom: 12px;
}
.type__title{
    font-weight: 500;
font-size: 14px;
line-height: 17px;
letter-spacing: 0.15px;
color: #2B2C3A;
margin-top: 12px;
}
.type__descr{
  font-weight: 400;
font-size: 12px;
line-height: 15px;
color: rgba(43, 44, 58, 0.5);
margin-top: 4px;  
}
.type__add__btn{
    display: flex;
    align-items: center;
    justify-content: center;
    background: none;
    border: none;
    font-weight: 400;
font-size: 12px;
line-height: 15px;
letter-spacing: 0.15px;
color: #6197FF;
margin: 0 auto;
    margin-top: 26px;
}
</style>

