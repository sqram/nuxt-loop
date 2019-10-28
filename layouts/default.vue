<template>
  <div>
    <nuxt />
    <Footer :locale=locale />
  </div>
</template>

<script>
import Footer from '~/components/Footer'

export default {
  components: {
    Footer
  },

  data () {
    return {
      locale: []
    }
  },

  async created () {
    let locale = await import ('~/locales/footer.js')
    this.locale = locale.default
  }
}
</script>