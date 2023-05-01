<template>
  <header>
    <nav>
      <div class="branding">
        <h1>FlashCards</h1>
      </div>
      <ul v-show="!mobile" class="navigation">
        <li><router-link class="link" :to="{ name: 'home' }">Home</router-link></li>
        <li><router-link class="link" :to="{ name: 'app' }">App</router-link></li>
        <li><router-link class="link" :to="{ name: 'about' }">About</router-link></li>
      </ul>
      <div class="icon">
        <i @click="toggleMobileNav" v-show="mobile" class="bi bi-view-list" :class="{ 'icon-active': mobileNav }"></i>
      </div>
      <transition name="mobile-nav">
        <ul v-show="mobileNav" class="dropdown-nav">
          <li><router-link @click="toggleMobileNav" class="link" :to="{ name: 'home' }">Home</router-link></li>
          <li><router-link @click="toggleMobileNav" class="link" :to="{ name: 'app' }">App</router-link></li>
          <li><router-link @click="toggleMobileNav" class="link" :to="{ name: 'about' }">About</router-link></li>
        </ul>
      </transition>
    </nav>
  </header>
</template>
<script>
export default {
  name: 'navigation',
  data() {
    return {
      mobile: false,
      isCollapsed: true,
      mobileNav: false,
      windowWidth: null
    }
  },
  created() {
    window.addEventListener('resize', this.checkScreen);
    this.checkScreen()
  },
  methods: {
    toggleMobileNav() {
      this.mobileNav = !this.mobileNav
    },

    checkScreen() {
      this.windowWidth = window.innerWidth
      if (this.windowWidth <= 768) {
        this.mobile = true
        return;
      }
      this.mobile = false
      this.mobileNav = false
      return;
    }
  },
  watch: {
    mobile() {
      console.log(this.mobile, this.mobileNav)
    }
  }
}
</script>
<style lang="scss" scoped>  * {
    margin: 0px;
    padding: 0px;
  }

  /* Header */
  header {
    background-color: rgba(70, 63, 58, 0.8);
    width: 100%;
    transition: 0.5s ease all;
    min-height: 83px;

    /* Navbar Global Configs */
    nav {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
/*       display: flex;
      flex-direction: row;
 */      width: 95%;
      margin: 0px 2%;
      padding-top: 1%;

      ul {
        margin-right: 5%;
      }

      ul,
      .link {
        justify-content: flex-end;
        text-decoration: none;
        list-style: none;
        color: var(--secondary-color);
        font-size: 30px;
      }

      li {
        margin: 0 8px;
        padding: 8px;
      }
    }

    /* Branding Config */
    .branding {
      justify-self: flex-start;
      color: var(--tertiary-color);
      margin: 1% 0;
    }

    /* Links Configs */
    .link {
      transition: 0.5s ease all;

      &:hover {
        color: var(--tertiary-color);
      }
    }

    /* Navigation Config */
    .navigation {
      grid-column-end: end;
      display: flex;
      align-items: center;
      flex: 1;
    }

    /* Icon Config */
    .icon {
      flex: 1;
      text-align: end;
      align-self: flex-end;

      i {
        font-size: 32px;
        color: var(--tertiary-color)
      }
    }
  }
  /* Mobile-nav Config */

  .mobile-nav-enter-active,
  .mobile-nav-leave-active {
    transition: 1s ease all;
  }

  .mobile-nav-enter-from,
  .mobile-nav-leave-to {
    transform: translateX(-350px);
  }
  .mobile-nav-enter-to {
    transform: translateX(0px);
  }

  /* Dropdown Config */
  .dropdown-nav {
    display: flex;
    flex-direction: column;
    position: fixed;
    background-color: var(--background-primary);
    width: 100%;
    max-width: 350px;
    height: 100%;
    top: 0;
    left: 0;
    justify-content: flex-start;
    padding-top: 1%;

    li:hover > .link {
      color: var(--tertiary-color);
      border-bottom: 1px solid var(--tertiary-color);
    }
  }

  .rotate-effect {
    transform: rotate(40deg);
  }
</style>