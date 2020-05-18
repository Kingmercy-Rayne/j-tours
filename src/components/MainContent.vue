<template>
  <main class="main">
    <h1>Wonderful Japan</h1>
    <div class="promotion__video">
      <button class="play__button"><i class="fas fa fa-play"></i></button>
      <div class="promotion__text">
        <h6>Promotion Video</h6>
        <h5><span>JAPAN</span> July 2009</h5>
      </div>
    </div>
    <button>Explore</button>
  </main>
</template>
<script>
export default {
  name: 'MainContent',
};
</script>

<style lang="stylus" scoped>
.main {
  z-index: 5;
  min-height: 50vh;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: space-between;
  margin-right: auto;
  padding: 2em;
  color: white;
  border: solid thin red;

  h1 {
    font-family: var(--font-family--alt);
    font-weight: 700;
    font-size: 3rem;
  }

  .promotion__video {
    display: flex;
    align-items: center;
    justify-content: space-between;
    border: solid thin var(--border-color--primary);
    padding: 0.3em 0;
    font-family: var(--font-family--alt);

    .play__button {
      text-align: center;
      border: solid thin var(--border-color--primary);
      border-radius: 50%;
      padding: 0.2em;
      margin: 0 1em;

      i {
        font-size: 0.8rem;
        padding: 0.2em;
      }
    }

    .promotion__text {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      justify-content: center;
      padding: 0.2em;
      text-align: center;
      font-family: var(--font-family--alt)
      font-weight:400;
      border: solid thin green;

      h5 {
        margin-top: 0.4em;
      }
    }
  }
}
</style>
