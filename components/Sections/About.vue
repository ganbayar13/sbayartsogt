<template>
  <div
    id="about"
    class="uk-child-width-1-2@m uk-grid-collapse"
    uk-grid
    uk-height-viewport
  >
    <div class="uk-cover-container">
      <img :src="require('@/assets/about.jpg')" alt="" uk-cover />
    </div>
    <div class="uk-section uk-section-muted" uk-height-viewport>
      <div class="uk-container">
        <h1
          class="uk-width-xlarge@m uk-heading-medium uk-text-uppercase"
          v-text="title"
        />
        <hr class="uk-width-xlarge@m uk-margin-medium" />
        <p class="uk-width-xlarge@m" v-text="description" />
        <h4 v-text="'БИД ЗӨВХӨН ХАМТАРЧ БАЙЖ ШИЙДЭЖ ЧАДНА.'" />
        <div class="uk-grid-small uk-child-width-1-2" uk-grid uk-margin>
          <div
            v-for="(item, i) in items"
            :key="i"
            class="uk-text-primary uk-text-uppercase uk-text-small"
          >
            <i uk-icon="icon: check" class="uk-margin-small-right" />
            {{ item }}
          </div>
        </div>
        <nuxt-link
          to="/about"
          class="uk-button uk-button-primary uk-margin-large-top"
          v-text="'Цааш унших'"
        />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    title: 'БИД АЖИЛЛАСААР Л БАЙНА БИДЭНТЭЙ НЭГДЭЭРЭЙ',
    description:
      'Яаж бид өрх бүрт өслтийг хүргэх вэ? Үндсэн хуулиа хэрхэн хамгаалж, ард түмэндээ үнэлэгдэж, хүндлэгдэх вэ? Энэ бүх үндсэн асуултууд бидний оюун санаанд олон жилийн туршид оршин тогтнож ирлээ. Одоо бидэнд тэдгээрт өгөх бүх хариулт байна. Бидэнтэй нэгдэж ирээдүйгээ өөрчил.',
    items: [
      'НЭГДСЭН ХЯНАЛТЫН ШИНЭЧЛЭЛТҮҮД',
      'ХУУЛЬ ЭРХ ЗҮЙ',
      'ГАДААД БОДЛОГО',
      'ЭДИЙН ЗАСАГ',
      'БОЛОВСРОЛ',
      'ЭРҮҮЛ МЭНД'
    ]
  })
}
</script>
<style scoped>
.bg {
  background-repeat: no-repeat;
  background-size: 50% 100%;
}
</style>
