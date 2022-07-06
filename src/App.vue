<template>
  <div id="app">
    <TheHeader></TheHeader>
    <BandNews></BandNews>
    <VideoPlayer></VideoPlayer>
    <LiveDates></LiveDates>
    <PhotoSlider></PhotoSlider>
    <KeepInContact></KeepInContact>
    <TheFooter></TheFooter>
  </div>
</template>

<script>

import TheHeader from './components/TheHeader.vue';
import BandNews from './components/BandNews.vue';
import TheFooter from './components/TheFooter.vue';
import VideoPlayer from './components/VideoPlayer.vue';
import LiveDates from './components/LiveDates.vue';
import PhotoSlider from './components/PhotoSlider.vue';
import KeepInContact from './components/KeepInContact.vue';



export default {
  name: 'App',
  components: { TheHeader, BandNews, TheFooter, VideoPlayer, LiveDates, PhotoSlider, KeepInContact }
}
</script>

<style lang="scss">
@import "assets/scss/main.scss";
#app {
  font-family: 'Montserrat', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: white;
  a {
    text-decoration: none;
  }
}
</style>
