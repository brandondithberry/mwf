<template>
  <div>
    <div class="announcement">
      <p>{{ info.announcement }} <nuxt-link to="/quote">Request a Quote</nuxt-link></p>
    </div>
    <header>
      <div class="container">
        <div>
          <nav>
            <ul>
              <li><nuxt-link to="/">Home</nuxt-link></li>
              <li><nuxt-link to="/repairs">Repairs</nuxt-link></li>
              <li><nuxt-link to="/lessons">Lessons</nuxt-link></li>
            </ul>
          </nav>
        </div>
        <div>
          <nuxt-link to="/"><img :src="info.sitelogo" alt="MWF Guitars Logo" class="logo" /></nuxt-link>
        </div>
        <div>
          <nav>
            <ul>
              <li><nuxt-link to="/portfolio">Portfolio</nuxt-link></li>
              <li><nuxt-link to="/about">About</nuxt-link></li>
              <li><nuxt-link to="/contact">Contact</nuxt-link></li>
            </ul>
          </nav>
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
  padding: 10px;
}

.logo {
  width: 120px;
}

header div,
nav ul {
  display: flex;
  place-content: center;
  place-items: center;
}

nav li a {
  padding: 10px;
  margin: 10px;
  color: black;
}

.cta {
  display: block;
  padding: 10px 20px;
  background: black;
  color: white;
}
</style>
