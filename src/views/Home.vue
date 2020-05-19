<template>
  <div class="home">
    <div class="backdrop__img">
      <img src="../assets/img/ismael-abelleira-MZ00oma1sn0-unsplash.jpg" alt="" />
    </div>
    <div class="backdrop__filter"></div>
    <section>
      <slide-bar />
      <main-content />
    </section>
    <the-infographic />
  </div>
</template>

<script>
// @ is an alias to /src
import MainContent from '@/components/MainContent.vue';
import SlideBar from '@/components/SlideBar.vue';
import TheInfographic from '@/components/TheInfographic.vue';

export default {
  name: 'Home',
  components: {
    MainContent,
    SlideBar,
    TheInfographic,
  },
};
</script>
<style lang="stylus" scoped>
.home {
  position: relative;
  // border: solid thin yellow;
  min-height: 100vh;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
  z-index: 0;
  padding-top: 6em;

  .backdrop__img {
    position: absolute;
    left: 0;
    top: 0;
    right: 0;
    bottom: 0;
    z-index: -10;

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: right bottom;
    }
  }

  .backdrop__filter {
    position: absolute;
    left: 0;
    top: 0;
    right: 0;
    bottom: 0;
    z-index: 0;
    background: rgba(0, 0, 0, 0.4);
  }

  section {
    // flex-grow: 1;
    min-height: 50vh;
    // border: solid thin crimson;
    display: flex;
    justify-content: center;
    align-items: center;
    // margin: 0 5%;
  }
}
</style>
