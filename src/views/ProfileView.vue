<template>
  <div class="ProfileView">
    <NavProfile/>
    <ProfileAcc/>
    <ProfileSeanse/>
    <ProfileAddChild/>
    <ProfileSupport/>
    <AboutApp/>
  </div>
</template>

<script>
import NavProfile from '@/components/NavProfile.vue';
import ProfileAcc from '@/components/ProfileAcc.vue';
import ProfileSeanse from '../components/ProfileSeanse.vue';
import ProfileAddChild from '../components/ProfileAddChild.vue';
import ProfileSupport from '../components/ProfileSupport.vue';
import AboutApp from '../components/AboutApp.vue';




export default {
  name: 'TrackHealth',
  components: {
    NavProfile,
    ProfileAcc,
    ProfileSeanse,
    ProfileAddChild,
    ProfileSupport,
    AboutApp
}
}
</script>

<style>

</style>

