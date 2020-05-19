<template>
  <div id="app">
    <the-navbar />
    <router-view />
  </div>
</template>
<script>
import TheNavbar from '@/components/TheNavbar.vue';

export default {
  components: {
    TheNavbar,
  },
};
</script>
<style lang="stylus">
#app {
  position: relative;
  width: 100%;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: var(--text-color--primary);
  overflow-x: hidden;
}
</style>
