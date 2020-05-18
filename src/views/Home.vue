<template>
  <div class="home">
    <div class="backdrop__img">
      <img src="../assets/img/jean-vella-AMUXeE7Y2Vc-unsplash.jpg" alt="" />
    </div>
    <div class="backdrop__filter"></div>
    <main class="main">swsws;lw;lsw;lw;</main>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
};
</script>
<style lang="stylus" scoped>
.home {
  position: relative;
  border: solid thin yellow;
  min-height: 100vh;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 0;

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
    }
  }

  .backdrop__filter {
    position: absolute;
    left: 0;
    top: 0;
    right: 0;
    bottom: 0;
    z-index: 0;
    background: rgba(0, 0, 0, 0.5);
  }

  .main {
    z-index: 5;
    color: white;
  }
}
</style>
