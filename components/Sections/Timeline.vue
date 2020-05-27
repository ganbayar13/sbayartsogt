<template>
  <div id="timeline" class="uk-section uk-section-default" uk-height-viewport>
    <div class="uk-container">
      <h1
        class="uk-heading-medium uk-text-center uk-text-uppercase uk-margin-remove"
        v-text="title"
      />
      <h5
        class="uk-text-primary uk-text-center uk-text-uppercase uk-margin-small-top bottom-line"
        v-text="subtitle"
      />
      <div class="uk-clearfix uk-margin-large-bottom" />
      <div
        class="uk-position-relative uk-visible-toggle"
        tabindex="-1"
        uk-slider="center: true"
      >
        <ul class="uk-slider-nav uk-dotnav uk-flex-center uk-margin"></ul>
        <div class="uk-slider-container">
          <ul
            class="uk-slider-items uk-child-width-1-2 uk-child-width-1-3@m uk-grid"
          >
            <li v-for="i in 10" :key="i">
              <div class="uk-inline uk-panel">
                <div class="uk-cover-container">
                  <img :src="require('@/assets/slide1.jpg')" alt="" uk-cover />
                  <canvas width="420" height="500" />
                </div>
                <div class="uk-overlay my-overlay uk-position-bottom">
                  <div>
                    <span
                      class="uk-label uk-label-secondary"
                      v-text="'MAY 16'"
                    />
                  </div>
                  <h3 class="white uk-margin-small-top">
                    "УРТ ЦАГААН” ҮЙЛЧИЛГЭЭНИЙ ТӨВИЙГ ДАХИН ТӨЛӨВЛӨХ
                  </h3>
                  <p class="white">
                    Нийслэлийн Засаг даргын 2020 оны А/520 дугаар захирамжийн
                    дагуу Нийслэлийн өмчийн гуравдугаар байр буюу...
                  </p>
                  <a
                    href="http://invest.ub.gov.mn/page/more/408"
                    target="_blank"
                    class="uk-button uk-button-primary"
                  >
                    Цааш унших
                  </a>
                </div>
              </div>
            </li>
          </ul>
        </div>

        <div class="uk-hidden@s uk-light">
          <a
            class="uk-position-center-left uk-position-small"
            href="#"
            uk-slidenav-previous
            uk-slider-item="previous"
          ></a>
          <a
            class="uk-position-center-right uk-position-small"
            href="#"
            uk-slidenav-next
            uk-slider-item="next"
          ></a>
        </div>

        <div class="uk-visible@s">
          <a
            class="uk-position-center-left-out uk-position-small"
            href="#"
            uk-slidenav-previous
            uk-slider-item="previous"
          ></a>
          <a
            class="uk-position-center-right-out uk-position-small"
            href="#"
            uk-slidenav-next
            uk-slider-item="next"
          ></a>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    title: 'Хөрөнгө оруулалт, бүтээн байгуулалт',
    subtitle:
      'Сэлэнгэ аймаг болон Монгол улсад хийж гүйцэтгэсэн бүтээн байгуулалтууд'
  })
}
</script>
<style scoped>
.my-overlay {
  background: rgba(0, 0, 0, 0)
    linear-gradient(rgba(0, 0, 0, 0), rgba(18, 31, 48, 0.8)) repeat scroll 0 0 !important;
}
.white {
  color: #ffffff !important;
}
</style>
