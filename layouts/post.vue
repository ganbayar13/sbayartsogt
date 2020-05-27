<template>
  <div>
    <div class="uk-position-relative">
      <img :src="require('@/assets/bg_top.jpg')" alt="bg_top" />
      <div class="uk-position-center">
        <div class="uk-container">
          <h2
            class="uk-light uk-text-center uk-text-white uk-text-uppercase"
            v-text="title"
          />
        </div>
      </div>
      <div class="uk-position-top">
        <div
          uk-sticky="animation: uk-animation-slide-top; sel-target: .uk-navbar-container; cls-active: uk-navbar-sticky hide-logo; cls-inactive: uk-navbar-transparent uk-light; top: 200"
        >
          <div class="uk-navbar-container">
            <div class="uk-container" uk-navbar>
              <div class="uk-navbar-left">
                <nuxt-link class="uk-navbar-item uk-logo" to="/">
                  <logo />
                </nuxt-link>
              </div>
              <div class="uk-navbar-right">
                <div class="uk-navbar-item uk-hidden@s">
                  <a
                    class="uk-navbar-toggle"
                    uk-navbar-toggle-icon
                    uk-toggle
                    href="#offcanvas"
                  />
                </div>
                <ul class="uk-navbar-nav uk-visible@m">
                  <li><nuxt-link to="/news/0">Нийтлэлүүд</nuxt-link></li>
                  <li><nuxt-link to="/news/0">Мэдээ мэдээлэл</nuxt-link></li>
                  <li><nuxt-link to="/about">Бидний тухай</nuxt-link></li>
                  <li><nuxt-link to="/manaibag">Манай баг</nuxt-link></li>
                  <li>
                    <nuxt-link to="/morynhotolbor">Мөрийн хөтөлбөр</nuxt-link>
                  </li>
                  <li><nuxt-link to="/namtar">Миний замнал</nuxt-link></li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <nuxt />
    <div class="uk-clearfix uk-margin" />
    <footer-section />
    <div id="offcanvas" uk-offcanvas="flip: true">
      <div class="uk-offcanvas-bar">
        <button class="uk-offcanvas-close" type="button" uk-close></button>

        <ul class="uk-nav-default" uk-nav>
          <li class="uk-active"><nuxt-link to="/">Эхлэл</nuxt-link></li>
          <li><nuxt-link to="/news/0">Нийтлэлүүд</nuxt-link></li>
          <li><nuxt-link to="/news/0">Мэдээ мэдээлэл</nuxt-link></li>
          <li><nuxt-link to="/about">Бидний тухай</nuxt-link></li>
          <li><nuxt-link to="/manaibag">Манай баг</nuxt-link></li>
          <li><nuxt-link to="/morynhotolbor">Мөрийн хөтөлбөр</nuxt-link></li>
          <li><nuxt-link to="/namtar">Миний замнал</nuxt-link></li>
        </ul>
        <hr />
        <div class="uk-margin">
          <input class="uk-input" type="text" placeholder="Хайлт" />
        </div>
        <div class="uk-position-bottom uk-position-medium">
          <ul class="uk-iconnav">
            <li><a href="#" uk-icon="icon: facebook"></a></li>
            <li><a href="#" uk-icon="icon: twitter"></a></li>
            <li><a href="#" uk-icon="icon: google"></a></li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Logo from '~/components/Logo'
import FooterSection from '~/components/Sections/FooterSection'
export default {
  components: { Logo, FooterSection },
  computed: {
    title: {
      get() {
        return this.$store.state.title
      }
    }
  }
}
</script>
<style scoped>
.hide-logo .uk-container .uk-navbar-left .uk-logo {
  display: none !important;
}
.hide-logo .uk-container .uk-navbar-right {
  /* margin-right: auto !important; */
}
.uk-text-white {
  color: #fff !important;
}
</style>
