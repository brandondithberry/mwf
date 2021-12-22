<template>
  <div class="banner" :style="{ background: bg }">
    <div class="overlay">
      <div class="inner">
        <h2>{{ title }}</h2>
        <h4>{{ subtitle }}</h4>
        <a class="btn" v-for="btn in button" :key="btn.text" :href="btn.link">{{ btn.text }}</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['title', 'subtitle', 'button', 'bg'],
}
</script>

<style scoped>
.banner {
  display: block;
  text-align: left;
  background-position: center;
  background-size: cover;
  max-width: 1920px;
  margin: 0 auto;
}

.overlay {
  display: block;
  background: linear-gradient(90deg, #000000cc, #00000000);
  width: 100%;
  height: 100%;
}

.inner {
  margin: 0 auto;
  padding: 14% 5%;
}

h2 {
  color: white;
  max-width: 440px;
}

h4 {
  color: white;
  margin-bottom: 40px;
  max-width: 440px;
}

.btn {
  display: inline;
  transition: 0.4s ease;
}

.btn:not(:last-child) {
  margin-right: 20px;
}
</style>  