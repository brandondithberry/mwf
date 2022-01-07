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
  transition: 0.4s ease;
  border: 2px solid #ab892f;
  box-sizing: content-box;
}

.image-text:after {
  filter: grayscale(100%);
}

.overlay {
  display: block;
  padding-top: 20%;
  background: #232122ee;
  width: 100%;
  height: 100%;
  transition: 0.4s ease;
}

.text {
  display: block;
  padding: 30px;
}

.image-text:hover {
  filter: grayscale(0%);
}

.image-text:hover .overlay {
  background: #23212299;
}

h2 {
  color: #fff;
}

h4 {
  color: #efefef;
  margin-top: 0;
}
</style>