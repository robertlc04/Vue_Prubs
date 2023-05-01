<template>
    <header :class="{ 'scrolled-nav': scrollPosition }">
      <nav>
        <div class="branding">
          <h1>FlashCards</h1>
        </div>
        <ul v-show="!mobile" class="navigation">
          <li><router-link class="link" :to="{ name: 'home'}">Home</router-link></li>
          <li><router-link class="link" :to="{ name: 'app'}">App</router-link></li>
          <li><router-link class="link" :to="{ name: 'about'}">About</router-link></li>
        </ul>
        <div class="icon">
          <i @click="toggleMobileNav" v-show="mobile" class="far fa-bars" :class="{'icon-active': mobileNav}"></i>
        </div>
        <transition name="mobile-nav">
          <ul v-show="mobileNav" class="dropdown-nav">
          <li><router-link class="link" :to="{ name: 'home'}">Home</router-link></li>
          <li><router-link class="link" :to="{ name: 'app'}">App</router-link></li>
          <li><router-link class="link" :to="{ name: 'about'}">About</router-link></li>
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
      isCollapsed: true
    }
  },
}
</script>
<style lang="scss" scoped>
  * {
    margin: 0px;
    padding: 0px;
  }

  header {
    background-color: rgba(70, 63, 58,0.8);
    z-index: 99;
    width: 100%;
    transition: 0.5s ease all;
    min-height: 83px;
    
    nav {
      display: flex;
      width: 95%;
      flex-direction: row;
      margin: 0px 2%;
      @media (min-width: 1140px) {
        max-width: auto;
      }
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
        margin: 1% 8px;
        padding: 8px;
      }
      
      .link {
        transition: 0.5s ease all;
        &:hover {
          color: var(--tertiary-color) ;
        }
      }
   
    
      .navigation {
        display: flex;
        align-items: center;
        flex: 1;
      }
    }
    
  }
  .branding {
    align-items: center;
    color: var(--tertiary-color);
    margin: 1% 0;
  }

</style>