<template>
  <div
    class="uk-section uk-section-secondary"
    :style="`background: #142236 url('${require('@/assets/footer_bg.png')}')`"
  >
    <div class="uk-text-center">
      <logo footer />
    </div>
    <div class="uk-text-center uk-margin-large-top">
      ThemeREX © 2020 All rights reserved. Terms of use and Privacy Policy
    </div>
  </div>
</template>
<script>
import Logo from '~/components/Logo'
export default {
  components: { Logo }
}
</script>
