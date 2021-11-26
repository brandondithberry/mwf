<template>
  <div class="image-text" :style="{ background: bg }">
    <nuxt-link :to="{ link }">
      <div class="overlay">
        <div class="inner">
          <h3>{{ heading }}</h3>
          <p>{{ description }}</p>
        </div>
      </div>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  props: ['heading', 'description', 'bg', 'link'],
}
</script>

<style scoped>
.image-text {
  text-align: left;
  border-radius: 10px;
  background-position: center;
  background-size: cover;
}

.overlay {
  display: block;
  border-radius: 10px;
  padding: 50% 30px 30px 30px;
  background: linear-gradient(#00000000, #000000cc);
  width: 100%;
  height: 100%;
}

a {
  border-radius: 10px;
}

h3 {
  color: white;
}

p {
  color: white;
}
</style>