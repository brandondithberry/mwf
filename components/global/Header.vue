<template>
  <div>
    <header>
      <div class="inside">
        <div class="logo-box">
          <nuxt-link to="/"><img :src="info.sitelogo" alt="MWF Guitars Logo" class="logo" /></nuxt-link>
        </div>
        <div>
          <a class="menu-icon">
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
    }
  },
}
</script>

<style lang="postcss" scoped>
header {
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
  background: #232122;
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

header .menu-icon:hover {
  height: 50px;
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
