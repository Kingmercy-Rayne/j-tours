<template>
  <nav class="nav">
    <div class="logo__container">
      <i><img src="" alt=""/></i>
      <span>JTours</span>
    </div>
    <ul>
      <li>Prices</li>
      <li>Our History</li>
      <li>Contact Us</li>
      <li>FAQ</li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'TheNavbar',
};
</script>
<style lang="stylus" scoped>
.nav {
  position: fixed;
  left: 0;
  top: 0;
  right: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  min-height: 10vh;
  padding: 0.2em;
  border: solid thin green;
  z-index: 10;
  color: var(--text-color--primary);

  .logo {
    padding: 1em;
    border: solid thin green;
  }

  ul {
    display: flex;
    justify-content: space-between;
    width: 40%;

    li {
      padding: 0 2em;
    }
  }
}
</style>
