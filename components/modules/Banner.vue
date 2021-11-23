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
  text-align: center;
  background-position: center;
  background-size: cover;
}

.overlay {
  display: block;
  background: #00000099;
  width: 100%;
  height: 100%;
}

.inner {
  max-width: 500px;
  margin: 0 auto;
  padding: 12% 20px;
}

h2 {
  color: white;
}

h4 {
  color: white;
  margin-bottom: 30px;
}

.btn {
  display: inline;
  padding: 15px 20px;
  background: black;
  color: white;
  border: none;
  margin: 10px;
}
</style>  