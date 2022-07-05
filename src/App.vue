<template>
  <div id="app">
    <!-- <nav class="d-flex justify-content-between align-items-center pt-3 px-5 my-navbar bg-dark">
      <img src="/img/avada-music-logo-retina.png" alt="" class="navbar-logo">
      <button @click="openMenu" class="navbar-toggle btn"><i class="fa-solid fa-bars fa-2x"></i></button>
    </nav> -->
    <TheHeader></TheHeader>
    <BandNews></BandNews>
    <VideoPlayer></VideoPlayer>
    <LiveDates></LiveDates>
    <PhotoSlider></PhotoSlider>
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



export default {
  name: 'App',
  components: { TheHeader, BandNews, TheFooter, VideoPlayer, LiveDates, PhotoSlider }
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
