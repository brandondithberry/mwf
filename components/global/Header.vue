<template>
  <header>
    <div class="announcement">
      <h5>{{ info.announcement }}</h5>
    </div>
    <div class="container">
      <div>
        <nav>
          <ul>
            <li><NuxtLink to="/">Home</NuxtLink></li>
            <li><NuxtLink to="/repairs">Repairs</NuxtLink></li>
            <li><NuxtLink to="/lessons">Lessons</NuxtLink></li>
          </ul>
        </nav>
      </div>
      <div>
        <NuxtLink to="/"><img :src="info.sitelogo" alt="MWF Guitars Logo" class="logo" /></NuxtLink>
      </div>
      <div>
        <nav>
          <ul>
            <li><NuxtLink to="/portfolio">Portfolio</NuxtLink></li>
            <li><NuxtLink to="/about">About</NuxtLink></li>
            <li><NuxtLink to="/contact">Contact</NuxtLink></li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
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
  padding: 10px;
}

.logo {
  width: 140px;
}

div,
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
