<template>
  <div id="start" class="uk-cover-container" uk-height-viewport>
    <img :src="require('@/assets/bg.jpg')" alt="" uk-cover />
    <div class="uk-overlay uk-position-center">
      <div class="uk-container-small">
        <div class="uk-margin-large-bottom uk-text-center">
          <logo />
        </div>
        <h5
          class="uk-text-primary uk-text-center uk-text-uppercase uk-margin-small-top bottom-line white-color"
          v-text="subtitle"
        />
        <h1
          class="uk-text-uppercase uk-text-center uk-heading-medium white-color"
          v-html="title"
        />
        <p
          class="uk-text-capitalize uk-text-center white-color"
          v-text="description"
        />
        <div class="uk-text-center uk-margin-large-top">
          <a class="uk-button uk-button-primary" v-text="'Цааш унших'" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Logo from '~/components/Logo'
export default {
  components: { Logo },
  data: () => ({
    title: 'Бид хамтдаа<br>түүхийг бүтээнэ',
    subtitle: 'Сэлэнгэ ялна',
    description: 'Өсөлтийг өрх бүрт'
  })
}
</script>
<style scoped>
.white-color {
  color: #ffffff !important;
}
</style>
