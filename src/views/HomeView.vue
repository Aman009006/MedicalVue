<template>
  <div class="home">
    <NavigationCont/>
    <MainNav/>
    <NavController/>
    <PopularThem/>
    <CategoryContent/>
    <ReagistrationModal/>
    <NewsContent/>
   
  </div>
</template>


<script>
// @ is an alias to /src

import MainNav from '../components/MainNav.vue'
import NavController from '@/components/NavController.vue'
import PopularThem from '@/components/PopularThem.vue'
import CategoryContent from '@/components/CategoryContent.vue'
import NewsContent from '@/components/NewsContent.vue'
import NavigationCont from '@/components/NavigationCont.vue'
import ReagistrationModal from '@/components/ReagistrationModal.vue'


export default {
  name: 'HomeView',
  components: {
    MainNav,
    NavController,
    PopularThem,
    CategoryContent,
    NewsContent,
    NavigationCont,
    ReagistrationModal
},
}
</script>

<style>
body{
  background: #E5E5E5;
}
navigation{
  background-color: white !important;
}
</style>

