<template>
  <div>
    <div class="uk-grid-collapse" uk-grid>
      <div class="uk-width-expand">
        <nuxt />
      </div>
      <div v-if="$route.name === 'index'" class="uk-width-auto uk-visible@m">
        <div style="width: 60px">
          <my-menu />
        </div>
      </div>
    </div>
    <socials />
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
import Menu from '~/components/Menu'
import Socials from '~/components/Socials'
export default {
  components: { MyMenu: Menu, Socials }
}
</script>
<style>
h1,
h2,
h3,
h4 {
  font-family: 'Old Standard TT' !important;
}
.bottom-line {
  position: relative;
  padding-bottom: 1.1em !important;
  letter-spacing: 2px !important;
}
.bottom-line:before {
  background: #1e87f0;
  bottom: 0;
  content: '';
  height: 1px;
  left: 50%;
  margin-left: -7px;
  position: absolute;
  width: 14px;
  z-index: 2;
}
.bottom-line:after {
  background: #e4e4e4;
  bottom: 0;
  content: '';
  height: 1px;
  left: 50%;
  margin-left: -40%;
  position: absolute;
  width: 80%;
}
.sidebar {
  background-color: #121f30;
  overflow: hidden;
}
</style>
