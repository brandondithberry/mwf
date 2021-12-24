<template>
  <div class="banner" :style="{ background: bg }">
    <div class="overlay">
      <div class="inner">
        <h1>{{ title }}</h1>
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
  max-width: 1440px;
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

h1 {
  color: white;
  max-width: 480px;
  line-height: 120%;
}

h4 {
  color: white;
  margin-bottom: 40px;
  max-width: 480px;
}

.btn {
  display: inline;
  transition: 0.4s ease;
}

.btn:not(:last-child) {
  margin-right: 20px;
}
</style>  