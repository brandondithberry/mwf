<template>
  <main>
    <section>
      <Banner :bg="bg" :title="title" :subtitle="subtitle" :button="button" />
    </section>
  </main>
</template>

<script>
import Banner from '~/components/modules/Banner'
export default {
  components: { Banner },
  data() {
    return {
      bg: "center / cover url('https://images.pexels.com/photos/4708872/pexels-photo-4708872.jpeg')",
      title: 'Reigniting the joy of owning and playing your guitar.',
      subtitle: 'Willis, Texas based Luthier  and Music Teacher providing guitar repair and service.',
      button: [
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