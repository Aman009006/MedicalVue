<template>
  <div class="MedCard">
    <NavigationCont/>
    <MedCardComponent/>
    <HealthCategory/>
  </div>
</template>

<script>
import NavigationCont from '@/components/NavigationCont.vue';
import MedCardComponent from '../components/MedCardComponent.vue';
import HealthCategory from '../components/HealthCategory.vue';


export default {
  name: 'HomeView',
  components: {
    NavigationCont,
    MedCardComponent,
    HealthCategory,
}
}
</script>

<style>

</style>

