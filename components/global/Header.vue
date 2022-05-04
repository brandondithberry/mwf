<template>
  <div>
    <Transition>
      <div class="fullpage-menu" v-if="showMobileMenu">
        <button type="button" class="close" @click="closeMenu">✕</button>
        <nav class="menu-box main-menu">
          <ul>
            <li><nuxt-link to="/">Home</nuxt-link></li>
            <li><nuxt-link to="/projects">Projects</nuxt-link></li>
            <li><nuxt-link to="/lessons">Lessons</nuxt-link></li>
            <li><nuxt-link to="/about">About</nuxt-link></li>
            <li><nuxt-link to="/contact">Contact</nuxt-link></li>
          </ul>
        </nav>
        <nav class="menu-box secondary-menu">
          <ul>
            <li><nuxt-link to="/repairs">Repairs</nuxt-link></li>
            <li><nuxt-link to="/maintenance">Maintenance</nuxt-link></li>
            <li><nuxt-link to="/customizations">Customizations</nuxt-link></li>
            <li><nuxt-link to="/replacement-parts">Replacement Parts</nuxt-link></li>
            <li><nuxt-link to="/upgrades">Upgrades</nuxt-link></li>
            <li><nuxt-link to="/consulting">Consulting</nuxt-link></li>
          </ul>
        </nav>
      </div>
    </Transition>
    <header>
      <div class="inside">
        <div class="logo-box">
          <nuxt-link to="/"><img :src="info.sitelogo" alt="MWF Guitars Logo" class="logo" /></nuxt-link>
        </div>
        <div>
          <a class="menu-icon" @click="openMenu">
            <span class="line"></span>
            <span class="line"></span>
            <span class="line"></span>
            <span class="line"></span>
            <span class="line"></span>
            <span class="line"></span>
            <span class="text">MENU</span>
          </a>
        </div>
      </div>
    </header>
  </div>
</template>

<script>
import info from '~/content/site/info.json'
export default {
  name: 'Header',

  data() {
    return {
      info: info,
      showMobileMenu: false,
    }
  },
  methods: {
    openMenu() {
      this.showMobileMenu = true
      document.body.style.overflow = 'hidden'
    },
    closeMenu() {
      this.showMobileMenu = false
      document.body.style.overflow = 'auto'
    },
  },
}
</script>

<style lang="postcss" scoped>
.v-enter {
  opacity: 0;
}

.v-enter-active,
.v-leave-active {
  transition: 0.4s ease-in-out;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}

.fullpage-menu {
  @apply fixed grid grid-cols-2 w-screen h-screen left-0 top-0 place-content-stretch bg-secondary-800 m-0 overflow-hidden z-50;
  overscroll-behavior: contain;

  .close {
    @apply absolute block right-5 top-5 text-4xl text-secondary-800;
  }

  a {
    @apply block text-secondary-100 text-4xl leading-loose border-b-2 border-secondary-800;
    transition: 0.4s ease;
  }

  a:hover,
  a.nuxt-link-active {
    @apply border-b-2 border-secondary-100 opacity-40;
  }

  .menu-box {
    @apply flex w-full h-full items-center justify-end p-20 text-right;
  }

  .secondary-menu {
    @apply justify-start bg-secondary-100 text-left;

    a {
      @apply text-dark text-3xl leading-loose;
    }
  }
}

header {
  @apply bg-dark;
  position: absolute;
  display: flex;
  top: 0;
  left: 0;
  width: 100%;
  height: 50px;
  margin: 0 auto;
  color: white;
  letter-spacing: 2px;
  place-items: center;
}

header div {
  display: flex;
}

header .inside {
  display: flex;
  place-content: space-between;
  align-items: flex-start;
  margin: 0 auto;
  width: 100%;
  height: 100%;
  max-width: 1240px;
  padding: 0 20px;
}

header .logo-box {
  padding: 10px;
  box-sizing: border-box;
}

header .logo {
  width: 120px;
}

header .menu-icon {
  display: block;
  height: 25px;
  cursor: pointer;
  color: white;
  transition: 0.4s ease;
}

header .menu-icon .text {
  display: block;
  background: #ab892f;
  color: #fff;
  border: 2px solid #ab892f;
  padding: 5px;
  width: 100%;
  text-align: center;
  margin: 0;
}

header .menu-icon .line {
  display: inline-block;
  background: #ddd;
  height: 100%;
  width: 2px;
  margin: 0;
}

header .menu-icon .line:not(:first-child) {
  margin-left: 6px;
}

header .menu-icon .line:nth-child(1) {
  width: 3px;
}

header .menu-icon .line:nth-child(2) {
  width: 2.6px;
}

header .menu-icon .line:nth-child(3) {
  width: 2.4px;
}

header .menu-icon .line:nth-child(4) {
  width: 2px;
}

header .menu-icon .line:nth-child(5) {
  width: 1.4px;
}

header .menu-icon .line:nth-child(6) {
  width: 1px;
}
</style>
