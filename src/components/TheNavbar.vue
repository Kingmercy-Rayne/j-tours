<template>
  <nav class="nav">
    <div class="logo__container">
      <img src="../assets/img/japan-flag-icon-16.png" alt="" />
      <!-- <span class="logo"> -->
      <!-- <img src="../assets/img/japan-flag-icon-16.png" alt="" /> -->
      <!-- </span> -->
      <span>JTours</span>
    </div>
    <ul>
      <li>Prices</li>
      <li>Our History</li>
      <li>Contact Us</li>
      <li>FAQ</li>
    </ul>
    <i class="fa fas fa-search search"></i>
    <div class="nav-toggle" @click="this.toggleSideNav">
      <span class="hamburger"></span>
    </div>
    <!-- sidepane -->
    <transition name="fade">
      <div :class="'sidepane__nav'" v-if="isSidepaneNavOpen">
        <div class="sidepane__nav--toggle" @click="this.toggleSideNav">
          <span class="hamburger"></span>
          <span class="hamburger__text">Close</span>
        </div>
        <ul class="nav-links">
          <li>Prices</li>
          <li>Our History</li>
          <li>Contact Us</li>
          <li>FAQ</li>
        </ul>
        <h2 class="brand-name">
          <router-link :to="'/'" @click.native="toggleSideNav">JTours</router-link>
        </h2>
      </div>
    </transition>
    <!-- End of sidepane -->
  </nav>
</template>

<script>
export default {
  name: 'TheNavbar',
  data() {
    return {
      isSidepaneNavOpen: false,
    };
  },
  computed: {
    isNotMobileScreen() {
      return this.windowWidth <= 768;
    },
  },
  methods: {
    toggleSideNav() {
      console.log(this.isNotMobileScreen);
      this.isSidepaneNavOpen = !this.isSidepaneNavOpen;
    },
  },
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
    padding: 0.2em 0.5em;
    // border: solid thin green;
    display: flex;
    align-items: center;

    @media screen and (max-width: 800px) {
      justify-self: flex-end;
    }

    // .logo {
    // border: solid thin white;
    // width: 1.2rem;
    // height: 1.1rem;
    // // padding:1em;
    // border-radius: 10%;

    // }
    img {
      width: 1.8rem;
      height: 1.8rem;
      border-radius: 50%;
      object-fit: cover;
      object-position: center center;
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

    @media screen and (max-width: 100px) {
      font-size: 0.7rem;
    }

    @media screen and (max-width: 800px) {
      display: none;
    }

    li {
      padding: 0 2em;
      font-size: 0.9rem;
      font-weight: 500;
    }
  }

  .search {
    margin: 0 3em;

    @media screen and (max-width: 800px) {
      display: none;
    }
  }

  .nav-toggle {
    width: 10%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-left: auto;
    cursor: pointer;
    margin: 1.2em;

    @media screen and (min-width: 800px) {
      display: none;
    }

    .hamburger {
      position: relative;
      display: block;

      &::before {
        content: '';
        position: absolute;
        top: 8px;
        left: 0.4em;
        right: 0;
      }

      &::after {
        content: '';
        position: absolute;
        bottom: 8px;
        left: 0.4em;
        right: 0;
      }
    }

    .hamburger, .hamburger::before, .hamburger::after {
      height: 0.15rem;
      width: 1.4rem;
      background: var(--text-color--primary);
    }
  }

  .sidepane__nav {
    // TODO: separate into component later
    position: absolute;
    top: 1px;
    left: 0;
    bottom: 1px;
    min-height: calc(100vh - 2px);
    width: 99%;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    padding: 0.5em;
    background: rgba(237, 237, 237, 0.99);
    filter: brightness(95%);
    transition: all 2s ease-in-out;
    overflow: scroll;
    color: black;

    .sidepane__nav--toggle {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1em;
      cursor: pointer;

      .hamburger__text {
        font-size: 0.8rem;
        font-weight: 500;
      }

      .hamburger {
        margin: 0 1.5em;
        position: relative;
        display: block;
        transform: translateY(0) rotate(135deg);

        &::before {
          content: '';
          position: absolute;
          bottom: 6px;
          transform: translateY(8px) translateX(-8px) rotate(-95deg);
        }
      }

      .hamburger, .hamburger::before {
        height: 0.12rem;
        width: 1.5rem;
        background: crimson;
      }
    }

    .brand-name {
      display: flex;
      padding: 0 2em;
      margin: 1em 0;
      justify-content: center;
      align-items: center;
      font-size: 2rem;
      font-weight: 800;
      font-family: var(--font-family--primary);
      flex-grow: 3;
    }

    .nav-links {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      flex-grow: 4;
      margin: 1em 1em;
      width: 100%;
      font-family: var(--font-family--alt);
      font-weight: 600;
      font-size: 1.2rem;

      li {
        padding: 1.4em 1em;
        margin: 0 1em;
        transition: all 0.05s ease-in-out;

        &:hover {
          transform: scale(1.1);
        }
      }
    }
  }

  // social
  .sidepane__nav__social {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    margin: 1em 0;

    .social-links {
      padding: 0.2em;

      i {
        padding: 1em 0.4em;
        font-size: 1.2rem;
        opacity: 1;
        transition: all 0.2s ease-in-out;

        &:hover {
          transform: scale(1.1);
        }
      }
    }

    span {
      flex-grow: 1;
      border: solid thin crimson;
      height: 2px;
      margin: 0.5em;
    }

    p {
      font-size: 0.7rem;
      font-weight: 600;
      letter-spacing: 2px;
    }
  }

  // style sidepane__nav transition
  .fade-enter-active, .fade-leave-active {
    transition: transform 0.4s cubic-bezier(0.68, -0.6, 0.32, 1.6);
  }

  .fade-enter, .fade-leave-to { /* .fade-leave-active below version 2.1.8 */
    transform: translateY(-100%);
  }
}
</style>
