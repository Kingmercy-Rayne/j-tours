<template>
  <div class="infographic">
    <div class="infographic__text">
      <span>.....</span>
      <h3>10 best spots to visit in Japan</h3>
      <button>More <i class="fa fas fa-long-arrow-right"></i></button>
    </div>
    <div class="infographic__img">
      <img src="../assets/img/jc3211-BpEH3K1G520-unsplash.jpg" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'TheInfographic',
};
</script>

<style lang="stylus" scoped>
.infographic {
  position: absolute;
  right: 0;
  bottom: 0;
  display: flex;
  align-items: center;
  justify-content: space-between;

  &:before {
    content: '';
    position: absolute;
    z-index: -10;
    right: 0;
    bottom: 0;
    top: 0;
    left: 0;
    background: rgba(0, 0, 0, 0.4);
  }

  .infographic__text {
    // border: solid thin brown;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    max-width: 40vw;
    padding: 1em;

    span {
      margin: 0.5em 0;
    }

    h3 {
      padding: 1em 0;
      word-break: 2rem;
    }

    button {
      border: none;
      padding-left: 0;

      i {
        padding: 0 1em;
      }
    }
  }

  .infographic__img {
    // border: solid thin green;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 10em;
    // padding:1em;
    width: 12em;
    margin: 0em 1em;

    // flex-grow: 1;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      filter: brightness(80%);
    }
  }
}
</style>
