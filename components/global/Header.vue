<template>
  <div>
    <header>
      <div>
        <nuxt-link to="/"><img :src="info.sitelogo" alt="MWF Guitars Logo" class="logo" /></nuxt-link>
      </div>
      <div>
        <a class="menu-icon">
          <span></span>
          <span></span>
          <span></span>
          <span></span>
          <span></span>
        </a>
      </div>
      <div>
        <nuxt-link to="quote" class="btn cta">Get a Quote</nuxt-link>
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
.announcement {
  background: #232122;
  padding: 10px;
  text-align: center;
}

.announcement p,
.announcement a {
  font-size: 0.9rem;
  color: white;
}

header {
  display: flex;
  padding: 10px;
  max-width: 1024px;
  margin: 0 auto;
  place-content: space-between;
  place-items: center;
}

header .menu-icon span {
  display: block;
  margin: 10px 0;
  background: black;
  width: 70px;
  height: 2px;
}

.logo {
  width: 120px;
}

header div,
nav ul {
  display: flex;
}

nav li a {
  padding: 10px;
  margin: 10px;
  color: black;
}

.cta {
  display: block;
  padding: 12px 25px;
}
</style>
