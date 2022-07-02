<template>
  <div class="track__content">
    <div class="container">
        <p class="track__title">Ваши трекеры</p>
        <div class="track__contents">
            <div class="track__text">
                <img src="../assets/images/icons/track__img.svg" alt="">
                <p class="track__titles">Базовый трекер</p>
                <p class="track__descr">Ты хорошо идешь, еще пару шагов, поднажми!</p>
            </div>
            <div class="track__tracking">
                <img src="../assets/images/icons/track__circle.svg" alt="" class="track__circle">
                    <svg class="progress-ring" width="90" height="90">
                        <circle class="progress-ring__circle" stroke="#FF6197" cx="45" cy="45" stroke-width="9"  r="40" fill="transparent"/>
                    </svg>
                    <p class="track__count">5/25</p>
            </div>
        </div>
  </div>
  </div>
</template>

<script>


export default {
  name: 'TrackContent',
  components: {},
  mounted() {
    this.circlePrecent()
  },
  methods:{
    circlePrecent(){
        const circle = document.querySelector('.progress-ring__circle');
        const radius = circle.r.baseVal.value;
        const circumference = 2 * Math.PI * radius;

        circle.style.strokeDasharray = `${circumference} ${circumference}`;
        circle.style.strokeDashoffset = circumference;

        function setProgress(percent) {
        const offset = circumference - percent / 100 * circumference;
        circle.style.strokeDashoffset = offset;
        }
        setProgress("40");
            }
        }
    }
</script>

<style>
.track__count{
    font-weight: 600;
font-size: 14px;
line-height: 150.02%;
display: flex;
align-items: center;
text-align: center;
color: rgba(43, 44, 58, 0.5);
position:absolute;
top:50%;
left:50%;
transform:translate(-50%, -50%);
}
.track__tracking{
    position: relative;
}
.progress-ring{
    position: absolute;
    top: 0;
    left: 0;
}
.progress-ring__circle {
  transform-origin: center;
  transform: rotate(-90deg);
  transition: storke-dashoffset 0.3s;
}
.track__title{
    font-weight: 600;
font-size: 20px;
line-height: 28px;
letter-spacing: 0.15px;
color: #2B2C3A;
margin-bottom: 14px;
}
.track__contents{
background: #FFFFFF;
padding: 12px;
box-shadow: 0px 2px 4px -2px rgba(24, 39, 75, 0.12), 0px 4px 4px -2px rgba(24, 39, 75, 0.08);
border-radius: 8px;
display: flex;
align-items: center;
justify-content: space-between;
}
.track__content{
    margin-top: 16px;
}
.track__text{
    max-width: 248px;
    width: 100%;
}
.track__titles{
    margin-top: 12px;
    font-weight: 500;
font-size: 14px;
line-height: 17px;
letter-spacing: 0.15px;
color: #2B2C3A;
}
.track__descr{
    font-weight: 400;
font-size: 12px;
line-height: 15px;
color: rgba(43, 44, 58, 0.5);
margin-top: 6px;
}
</style>

