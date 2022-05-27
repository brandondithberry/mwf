<template>
  <footer>
    <section class="contact" id="connect">
      <div>
        <h2>Get In Touch</h2>
        <p>
          MWF would love to make your guitar dreams a reality, whether that's bringing a customization to life, or
          advancing your skills in playing your guitar or bass. Let us know how we can help.
        </p>
        <h4><b>Get a Quote</b></h4>
        <h5>Use the form or give us a call at (936) 123-4567.</h5>
      </div>
      <div>
        <form name="Contact" method="POST" data-netlify="true" netlify>
          <label class="hidden"> Don’t fill this out if you’re human: <input name="bot-field" /> </label>
          <label for="name">Full Name</label>
          <input class="p-2" type="text" id="name" name="name" placeholder="Your name.." />

          <label for="email">Email</label>
          <input class="p-2" type="text" id="email" name="email" placeholder="Your email.." />

          <label for="subject">Message</label>
          <textarea
            class="p-2"
            id="subject"
            name="subject"
            placeholder="How can I help?"
            style="height: 200px"
          ></textarea>

          <input class="btn" type="submit" value="Send" />
        </form>
      </div>
    </section>
    <section class="navigation">
      <div class="logo">
        <nuxt-link to="/"><img src="/img/mwf-guitars-logo.png" alt="Footer MWF Logo" /></nuxt-link>
      </div>
      <div class="menu">
        <nav>
          <nuxt-link to="/"><p>Home</p></nuxt-link>
          <nuxt-link to="/#connect"><p>Get In Touch</p></nuxt-link>
          <nuxt-link to="/privacy-policy"><p>Privacy Policy</p></nuxt-link>
          <nuxt-link to="/terms-of-service"><p>Terms of Service</p></nuxt-link>
        </nav>
      </div>
      <div class="copyright">
        <p>Copyright &copy; 2022 MWF Guitars & Music</p>
      </div>
    </section>
  </footer>
</template>

<style lang="postcss" scoped>
.contact {
  @apply grid grid-cols-1 lg:grid-cols-2 bg-secondary-600 my-4 lg:my-6;

  div {
    @apply p-8 lg:p-20;
  }

  div:nth-child(1) {
    @apply bg-white;

    h2,
    h5,
    h4,
    p {
      @apply text-dark;
    }
  }

  form {
    input,
    textarea {
      @apply w-full block mb-4;
    }
  }
}

.navigation {
  @apply flex w-full place-items-stretch place-content-between p-4 gap-10 flex-col lg:flex-row;

  .logo {
    @apply flex place-items-center place-content-center flex-col lg:flex-row;

    img {
      @apply w-full;
      max-width: 120px;
    }
  }

  .menu {
    @apply flex flex-col lg:flex-row;

    nav {
      @apply flex place-items-center place-content-center gap-10 flex-col lg:flex-row;

      p {
        @apply text-white;
      }
    }
  }

  .copyright {
    @apply flex justify-end items-center place-content-center flex-col lg:flex-row;
  }
}
</style>

<script>
export default {}
</script>