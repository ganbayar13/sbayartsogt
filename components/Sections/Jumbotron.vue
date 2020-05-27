<template>
  <div class="uk-cover-container" uk-height-viewport>
    <img :src="require('@/assets/bg.jpg')" alt="" uk-cover />
    <div class="uk-overlay uk-position-top-center uk-position-large">
      <logo />
    </div>
    <div class="uk-overlay uk-position-center">
      <div class="uk-container-small">
        <h5
          class="uk-text-primary uk-text-center uk-text-uppercase uk-margin-small-top bottom-line white-color"
          v-text="subtitle"
        />
        <h1
          class="uk-text-uppercase uk-text-center uk-heading-large white-color"
          v-text="title"
        />
        <p
          class="uk-text-capitalize uk-text-center white-color"
          v-text="description"
        />
        <div class="uk-text-center uk-margin-large-top">
          <a class="uk-button uk-button-primary" v-text="'Learn more'" />
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
    title: 'We will make history together',
    subtitle: 'justify & honesty',
    description: 'We must come together once again'
  })
}
</script>
<style scoped>
.white-color {
  color: #ffffff !important;
}
</style>
