<template>
  <img :data-src="img" alt="logo" uk-img />
</template>
<script>
export default {
  props: {
    footer: {
      type: Boolean,
      default: false
    }
  },
  computed: {
    img: {
      get() {
        if (this.footer) {
          return require('@/assets/logo_footer.png')
        }
        return require('@/assets/logo.png')
      }
    }
  }
}
</script>
