<template>
  <main>
    <section>
      <Banner
        :bg="'0% 60% / 170% url(\'https://images.pexels.com/photos/4708872/pexels-photo-4708872.jpeg\')'"
        :title="'Reigniting the joy of owning and playing your guitar.'"
        :subtitle="'Willis, Texas based Luthier  and Music Teacher providing guitar repair and service.'"
        :button="heroButtons"
      />
    </section>
    <section>
      <div class="flex place-content-center gap-6 p-14">
        <image-text
          :bg="'0% 60% / 170% url(\'~/static/img/clamped-acoustic.jpg\')'"
          :heading="'Please mom'"
          :description="'Don\'t make me put my laptop away.'"
        />
        <image-text
          :bg="'0% 60% / 170% url(\'https://images.pexels.com/photos/4708872/pexels-photo-4708872.jpeg\')'"
          :heading="'Please mom'"
          :description="'Don\'t make me put my laptop away.'"
        />
        <image-text
          :bg="'0% 60% / 170% url(\'https://images.pexels.com/photos/4708872/pexels-photo-4708872.jpeg\')'"
          :heading="'Please mom'"
          :description="'Don\'t make me put my laptop away.'"
        />
      </div>
    </section>
  </main>
</template>

<script>
import Banner from '~/components/modules/Banner'
import ImageText from '~/components/modules/ImageText'

export default {
  components: { Banner, ImageText },
  data() {
    return {
      heroButtons: [
        {
          text: 'Request a Quote',
          link: '/quote',
        },
        {
          text: 'View Portfolio',
          link: '/portfolio',
        },
      ],
    }
  },
}
</script>