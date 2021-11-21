<template>
  <header>
    <div class="container">
      <div>
        <NuxtLink to="/"><img :src="info.sitelogo" alt="MWF Guitars Logo" class="logo" /></NuxtLink>
      </div>
      <div class="menu">
        <nav>
          <ul>
            <li><NuxtLink to="/">Home</NuxtLink></li>
            <li><NuxtLink to="/repairs">Repairs</NuxtLink></li>
            <li><NuxtLink to="/lessons">Lessons</NuxtLink></li>
            <li><NuxtLink to="/work">Work</NuxtLink></li>
            <li><NuxtLink to="/about">About</NuxtLink></li>
            <li><NuxtLink to="/contact">Contact</NuxtLink></li>
          </ul>
        </nav>
      </div>
      <div><NuxtLink to="/quote" class="cta">Get A Quote</NuxtLink></div>
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
  padding: 20px;
}

.logo {
  width: 140px;
}

div,
nav ul {
  display: flex;
  align-content: center;
  align-items: center;
  justify-content: space-between;
  justify-items: space-between;
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
