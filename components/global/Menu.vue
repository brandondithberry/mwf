<template>
  <div class="fullpage-menu">
    <nav>
      <ul>
        <li><nuxt-link to="/">Home</nuxt-link></li>
        <li>
          <ul>
            <li><nuxt-link to="/repairs">Repairs</nuxt-link></li>
            <li><nuxt-link to="/maintenance">Maintenance</nuxt-link></li>
            <li><nuxt-link to="/customizations">Customizations</nuxt-link></li>
            <li><nuxt-link to="/parts-upgrades">Parts & Upgrades</nuxt-link></li>
            <li><nuxt-link to="/consulting">Consulting</nuxt-link></li>
          </ul>
        </li>
        <li><nuxt-link to="/projects">Projects</nuxt-link></li>
        <li><nuxt-link to="/lessons">Lessons</nuxt-link></li>
        <li><nuxt-link to="/about">About</nuxt-link></li>
        <li><nuxt-link to="/contact">Contact</nuxt-link></li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Menu',
}
</script>

<style lang="postcss">
.fullpage-menu {
  @apply fixed flex place-content-stretch place-items-stretch z-50 bg-secondary;

  li {
    @apply text-white;
  }
}
</style>