<template>
  <div class="TrackHealth">
   <NavigationCont/>
   <TrackerContent/>
   <TrackerSlider/>
   <TrackingTypes/>
  </div>
</template>

<script>
import NavigationCont from '@/components/NavigationCont.vue';
import TrackerContent from '../components/TrackerContent.vue';
import TrackerSlider from '../components/TrackerSlider.vue';
import TrackingTypes from '@/components/TrackingTypes.vue';



export default {
  name: 'TrackHealth',
  components: {
    NavigationCont,
    TrackerContent,
    TrackerSlider,
    TrackingTypes
}
}
</script>

<style>

</style>

