<template>
  <div>
    <jumbotron />
    <services />
    <about />
    <what-is-new />

    <div class="uk-grid-collapse uk-child-width-1-2@m" uk-grid>
      <div class="uk-section uk-section-small uk-section-custom uk-text-center">
        <a href="#" class="uk-button uk-button-text"
          ><h4 class="uk-margin-remove uk-text-uppercase">
            Таньд тулгамдсан ямар асуудал байна?
          </h4></a
        >
      </div>
      <div
        class="uk-section uk-section-small uk-section-primary uk-flex uk-flex-around"
      >
        <div>
          <h4
            class="uk-margin-remove uk-text-uppercase"
            v-text="'Биднийг дагаарай'"
          />
        </div>
        <div>
          <ul class="uk-iconnav">
            <li><a href="" uk-icon="icon: facebook"></a></li>
            <li><a href="" uk-icon="icon: twitter"></a></li>
            <li><a href="" uk-icon="icon: google"></a></li>
          </ul>
        </div>
      </div>
    </div>

    <magazine />
    <timeline />
    <contact-us />
    <footer-section />
  </div>
</template>
<script>
import Jumbotron from '~/components/Sections/Jumbotron'
import Services from '~/components/Sections/Services'
import About from '~/components/Sections/About'
import WhatIsNew from '~/components/Sections/WhatIsNew'
import Magazine from '~/components/Sections/Magazine'
import FooterSection from '~/components/Sections/FooterSection'
import Timeline from '~/components/Sections/Timeline'
import ContactUs from '~/components/Sections/ContactUs'
export default {
  components: {
    Jumbotron,
    Services,
    About,
    WhatIsNew,
    FooterSection,
    Magazine,
    Timeline,
    ContactUs
  }
}
</script>
<style scoped>
.uk-section-custom {
  background-color: rgb(255, 183, 0) !important;
}
</style>
