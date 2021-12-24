<template>
  <div class="image-text" :style="{ background: bg }">
    <nuxt-link :to="{ link }">
      <div class="overlay" :style="{ background: overlay }">
        <div class="text">
          <h2>
            <b>{{ heading }}</b>
          </h2>
          <h4>{{ description }}</h4>
        </div>
      </div>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  props: ['heading', 'description', 'bg', 'overlay', 'link'],
}
</script>

<style scoped>
.image-text {
  text-align: left;
  background-position: center;
  background-size: cover;
  filter: saturate(0%);
  transition: 0.4s ease;
}

.overlay {
  display: block;
  padding: 20% 0;
  background: #232122dd;
  width: 100%;
  height: 100%;
  transition: 0.4s ease;
}

.text {
  display: block;
  padding: 30px;
}

.image-text:hover {
  filter: saturate(100%);
}

.image-text:hover .overlay {
  background: #232122bb;
}

h2 {
  color: #fff;
}

h4 {
  color: #efefef;
  margin-top: 0;
}
</style>