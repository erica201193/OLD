<template>
  <div id="app">
    <TheHeader></TheHeader>
    <TheMain></TheMain>
    <VideoPlayer></VideoPlayer>
    <LiveDates></LiveDates>
    <TheFooter></TheFooter>
  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheMain from './components/TheMain.vue';
import TheFooter from './components/TheFooter.vue';
import VideoPlayer from './components/VideoPlayer.vue';
import LiveDates from './components/LiveDates.vue';

export default {
  name: 'App',
  components: { TheHeader, TheMain, TheFooter, VideoPlayer, LiveDates }
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
