<template>
  <div class="image-text" :style="{ background: bg }">
    <nuxt-link :to="{ link }">
      <div class="overlay">
        <h4>
          <b>{{ heading }}</b>
        </h4>
        <p>{{ description }}</p>
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
  padding: 70% 30px 30px 30px;
  background: linear-gradient(20deg, #000000ee, #00000000);
  width: 100%;
  height: 100%;
}

a {
  border-radius: 10px;
}

h4 {
  color: white;
}

p {
  margin-top: 0;
}
</style>