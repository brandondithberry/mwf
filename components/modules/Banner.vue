<template>
  <div class="banner" :style="{ background: bg }">
    <div class="overlay">
      <div class="inner">
        <div class="text">
          <h1>{{ title }}</h1>
          <h4>{{ subtitle }}</h4>
        </div>
        <div class="btns">
          <a class="btn" v-for="btn in button" :key="btn.text" :href="btn.link">{{ btn.text }}</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['title', 'subtitle', 'button', 'bg'],
}
</script>

<style lang="postcss" scoped>
.banner {
  @apply flex h-auto place-content-center place-items-center;
  background-position: center;
  background-size: cover;
  margin: 0 auto;
}

.overlay {
  @apply flex w-full h-full p-20 place-content-center items-center justify-start lg:py-48;
  background: linear-gradient(90deg, #000000cc, #00000000);
}

.inner {
  @apply max-w-xl text-white;
}
</style>