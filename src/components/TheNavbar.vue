<template>
  <nav class="nav">
    <div class="logo__container">
      <span class="logo">
        <img src="../assets/img/japan-flag-icon-16.png" alt="" />
      </span>
      <span>JTours</span>
    </div>
    <ul>
      <li>Prices</li>
      <li>Our History</li>
      <li>Contact Us</li>
      <li>FAQ</li>
    </ul>
    <i class="fa fas fa-search search"></i>
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
  // border: solid thin green;
  z-index: 10;
  color: var(--text-color--primary);

  .logo__container {
    padding: 0.2em;
    border: solid thin green;
    display: flex;
    align-items: center;

    .logo {
      border: solid thin white;
      width: 1.2rem;
      height: 1.1rem;
      // padding:1em;
      border-radius: 10%;

      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }

    span {
      padding: 1em;
    }
  }

  ul {
    display: flex;
    justify-content: space-between;
    width: 40%;
    margin: 0 4em;
    margin-left: auto;

    li {
      padding: 0 2em;
      font-size: 0.9rem;
      font-weight: 500;
    }
  }

  .search {
    margin: 0 3em;
  }
}
</style>
