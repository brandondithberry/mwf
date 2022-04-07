<template>
  <div class="image-text">
    <div v-if="type == 'over'" class="over" :style="{ background: bg }">
      <nuxt-link :to="{ link }">
        <div class="overlay" :style="{ background: overlay }">
          <div class="text">
            <h3>
              <b>{{ heading }}</b>
            </h3>
            <h4>{{ description }}</h4>
          </div>
        </div>
      </nuxt-link>
    </div>
    <div v-if="type == 'bottom'" class="bottom">
      <nuxt-link :to="{ link }">
        <div class="image" :style="{ backgroundImage: bg }"></div>
        <div class="text">
          <h3>
            <b>{{ heading }}</b>
          </h3>
          <h4>{{ description }}</h4>
        </div>
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    heading: String,
    description: String,
    bg: String,
    link: String,
    type: {
      default: 'over',
      type: String,
    },
  },
}
</script>

<style lang="postcss" scoped>
.image-text {
  @apply flex w-full h-full place-content-stretch place-items-stretch;
}

.bottom {
  @apply w-full h-full;

  .image {
    @apply w-full h-full;
    background: no-repeat center center / cover;
    height: 200px;
  }

  .text {
    @apply w-full bg-secondary text-dark p-6;

    h2,
    h4 {
      @apply m-0;
    }
  }
}

.overlay {
  @apply w-full h-full;
  background: #00000077;
  transition: 0.4s ease;
}

.overlay:hover {
  background: #00000000;
  backdrop-filter: scale(1.5);
}
</style>