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
      <div class="grid gap-4 py-4 grid-cols-1 lg:grid-cols-4 lg:gap-8 lg:py-8">
        <image-text
          :bg="'url(\'https://images.unsplash.com/photo-1519423836910-49d53e49398c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80\')'"
          :heading="'Repair & Cleaning'"
          :description="'Expert luthier services'"
          :type="'bottom'"
        />
        <image-text
          :bg="'url(https://images.pexels.com/photos/7520779/pexels-photo-7520779.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1)'"
          :heading="'Music Lessons'"
          :description="'Rekindle your passion'"
          :type="'bottom'"
        />
        <image-text
          :bg="'url(\'https://images.unsplash.com/photo-1545560556-520cd73f3886?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1925&q=80\')'"
          :heading="'Customizations'"
          :description="'Bring your dreams to life'"
          :type="'bottom'"
        />
        <image-text
          :bg="'url(\'https://images.unsplash.com/photo-1588616531352-7a03ceda0003?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1025&q=80\')'"
          :heading="'Parts & Upgrades'"
          :description="'High quality installation'"
          :type="'bottom'"
        />
      </div>
    </section>
    <section class="about">
      <div class="box">
        <h2 class="text-primary">★★★★★</h2>
        <h3>Known for Delivering Excellence</h3>
        <p>
          Since 2017, MWF Guitars & Music has become a well-renowned Guitar Repair Service in Conroe, Texas. What
          started out as a hobby turned into a full-fledged business offering the highest quality repairs at affordable
          prices. Our passion for fixing what's broken has brought us to the forefront of the repair industry, and our
          impeccable results have kept us there.
        </p>
      </div>
      <div class="box"></div>
    </section>
    <section class="testimonials">
      <div class="testimony">
        <figure>
          <div class="dots">
            <div>•</div>
            <div>•</div>
            <div>•</div>
            <div>•</div>
            <div>•</div>
            <div>•</div>
          </div>
          <blockquote>
            "After horrible service elsewhere, I came here and cannot say enough good things about Melvin's guitar
            repair services!"
          </blockquote>
          <figcaption>J. Brown</figcaption>
        </figure>
      </div>
      <div class="testimony">
        <figure>
          <div class="dots">
            <div>•</div>
            <div>•</div>
            <div>•</div>
            <div>•</div>
            <div>•</div>
            <div>•</div>
          </div>
          <blockquote>
            "MWF Guitars is the only place you should trust with your guitar. Top notch work and excellent service."
          </blockquote>
          <figcaption>C. Copeland</figcaption>
        </figure>
      </div>
      <div class="testimony">
        <figure>
          <div class="dots">
            <div>•</div>
            <div>•</div>
            <div>•</div>
            <div>•</div>
            <div>•</div>
            <div>•</div>
          </div>
          <blockquote>"Melvin is a phenomenal instructor! My son looks forward to his weekly bass lessons!"</blockquote>
          <figcaption>J. Stark</figcaption>
        </figure>
      </div>
    </section>
    <section>
      <Banner
        :bg="'0% 60% / 170% url(\'https://images.pexels.com/photos/4088015/pexels-photo-4088015.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1\')'"
        :title="'Make your guitar your own with MWF customizations, upgrades and setups.'"
        :subtitle="'MWF works with you to perfect your setup including the action, intonation and other aspects, ensuring you love the feel and sound of your guitar.'"
        :button="heroButtons"
      />
    </section>
  </main>
</template>

<style lang="postcss" scoped>
.about {
  @apply flex w-full place-items-stretch place-content-center flex-col lg:flex-row;

  .box {
    @apply p-6 bg-white lg:w-1/2 lg:p-20;

    h3,
    p {
      @apply text-dark;
    }
  }

  .box:nth-child(2) {
    @apply p-20;
    background: no-repeat center center / cover
      url('//images.pexels.com/photos/1539787/pexels-photo-1539787.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1');
  }
}

.testimonials {
  @apply grid grid-cols-1 gap-4 py-4 lg:grid-cols-3 lg:gap-6 lg:py-6 place-content-stretch place-items-stretch;

  .testimony {
    @apply p-8 bg-gray-100 text-dark text-center lg:p-10;

    .dots {
      @apply flex place-content-stretch place-items-stretch mb-4 p-0 text-5xl text-gray-300 leading-5;

      div {
        @apply w-1/6;
      }
    }

    blockquote {
      @apply mb-2 text-lg italic;
    }

    figcaption {
      @apply text-xl font-bold;
    }
  }
}
</style>

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
          link: '#connect',
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