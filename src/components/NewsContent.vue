<template>
<div class="news__content">
    <div class="container">
        <div class="news__titls">
          <p class="news__titles">Новости сайта</p>
          <a href="#" class="arrow"> <img src="../assets/images/avec.svg" alt=""></a>
        </div>

     <div v-for="n in news" :key="n.title" class="news">
      <img :src="n.image" alt="" class="news__img">
      <div class="news__text">
        <p class="news__title">{{ n.title }}</p>
        <p class="news__date">{{n.created_at}}</p>
      </div>
     </div>

      <button v-if="count > news.length" @click="warn" class="category__btn">
        Посмотреть все
      </button>

    </div>
</div>
</template>

<script>
import axios from 'axios'
  export default {
  name: 'NewsContent',
  props: {
    msg: String
  },
  data: () => ({
    news: [],
    count: 0,
    page: 1,
    pageSize: 2
  }),

  async mounted() {
    const { results, count } = await this.getNews()
    this.news = results
    this.count = count
  },
  methods: {
    async getNews() {
      try {
        const params = {
          page: this.page,
          page_size: this.pageSize
        }
        const { data } = await axios.get('https://api.checkin.kg/api/v1/news', { params })
        return data
      } catch (e) {
        console.error(e)
      }
    },
    async warn() {
      this.pageSize = this.pageSize + 2
      const { results } = await this.getNews()
      this.news = results
    }
  }
}
</script>

<style >
.news__content{
  margin-top: 24px;
  margin-bottom: 74px;
}
.news__titls{
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 12px;
}
.news__titles{
  font-weight: 600;
font-size: 20px;
line-height: 28px;
letter-spacing: 0.15px;
color: #2B2C3A;
border-radius: 2px;
}
.news{
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: white;
margin-bottom: 12px;
  border-radius: 15px;
}
.news__img{
  border-top-left-radius:15px;
  border-bottom-left-radius:15px;
  max-width: 136px;
  width: 100%;
  height: 90px;
}
.news__title{
 font-weight: 400;
font-size: 14px;
line-height: 20px;
letter-spacing: 0.005em;
color: #2B2C3A;
margin-bottom: 8px;
}
.news__text{
  width: 218px;
  padding: 12px;
  
}
.news__date{
  font-weight: 400;
font-size: 14px;
line-height: 17px;
letter-spacing: 0.1px;
color: rgba(43, 44, 58, 0.5);
}
</style>
