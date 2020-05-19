<template>
  <div class="slidebar"></div>
</template>

<script>
export default {
  name: 'SlideBar',
};
</script>

<style lang="stylus" scoped>
.slidebar {
  position: relative;
  height: 30vh;
  width: 0.2rem;
  margin: 2em 4em;
  background: #555;

  @media screen and (max-width: 1000px) {
    margin: 2em 2em;
  }

  &:before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 30%;
    background: #ddd;
  }

  &:after {
    content: '03';
    position: absolute;
    bottom: -2em;
    transform: translate(-50%, 0);
    font-size: 0.8rem;
  }
}
</style>
