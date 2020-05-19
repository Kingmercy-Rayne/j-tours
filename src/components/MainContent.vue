<template>
  <main class="main">
    <h1>
      <span>Wonderful </span>
      <span>Japan</span>
    </h1>
    <div class="promotion__video">
      <button class="play__button"><i class="fas fa fa-play"></i></button>
      <div class="promotion__text">
        <h6>Promotion Video</h6>
        <h5><span>JAPAN</span> July 2009</h5>
      </div>
    </div>
    <button class="cta-btn">Explore</button>
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
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: space-between;
  // margin-right: auto;
  padding: 0 2em;
  // border: solid thin green;
  color: white;

  h1 {
    font-family: var(--font-family--alt);
    font-weight: 800;
    font-size: 4rem;
    // line-height: 4rem;
    letter-spacing: 1.5px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }

  .promotion__video {
    display: flex;
    align-items: center;
    justify-content: space-between;
    // border: solid thin var(--border-color--primary);
    padding: 0.3em 0;
    margin: 2.2em 0;
    font-family: var(--font-family--alt);

    .play__button {
      text-align: center;
      border: solid thin var(--border-color--primary);
      border-radius: 50%;
      padding: 0.4em;
      margin-right: 1em;

      i {
        font-size: 0.8rem;
        padding: 0.4em;
      }
    }

    .promotion__text {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      justify-content: center;
      padding: 0.2em;
      text-align: center;
      font-family: var(--font-family--alt);
      font-weight: 400;

      h5 {
        margin-top: 0.4em;
      }
    }
  }

  .cta-btn {
    background: var(--button-bg-color--primary);
    border: none;
    border-radius: 0.5em;
  }
}
</style>
