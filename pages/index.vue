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
      <div class="contain grid-cols-3 gap-7 py-16">
        <image-text
          :bg="'50% 80% / 100% url(\'/img/clamped-acoustic.jpg\')'"
          :heading="'Repair & Cleaning'"
          :description="'Expert luthier services.'"
        />
        <image-text
          :bg="'0% 100% / 100% url(\'/img/lessons.jpg\')'"
          :heading="'Music Lessons'"
          :description="'Rekindle your passion.'"
        />
        <image-text
          :bg="'50% 80% / 100% url(\'/img/custom.jpg\')'"
          :heading="'Customizations'"
          :description="'Bring your dreams to life.'"
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