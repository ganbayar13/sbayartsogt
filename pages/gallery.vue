<template>
  <div>
    <div class="uk-container uk-container-small uk-margin-top">
      <div
        class="uk-child-width-1-3@m uk-child-width-1-2@s"
        uk-grid
        uk-lightbox
      >
        <div v-for="(item, i) in items" :key="i">
          <div class="uk-inline">
            <img :data-src="item.src" alt="" uk-img />
            <div
              class="uk-overlay uk-overlay-default uk-position-bottom uk-padding-small"
            >
              <span v-text="item.description" />
            </div>
            <a
              :href="item.src"
              class="uk-overlay uk-position-cover"
              :data-caption="item.description"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  layout: 'post',
  data: () => ({
    title: 'Зургийн цомог',
    items: [
      { src: require('@/assets/gallery/1.jpg'), description: 'tailbar 1' },
      { src: require('@/assets/gallery/2.jpg'), description: 'tailbar 2' },
      { src: require('@/assets/gallery/3.jpg'), description: 'tailbar 3' },
      { src: require('@/assets/gallery/4.jpg'), description: 'tailbar 4' },
      { src: require('@/assets/gallery/5.jpg'), description: 'tailbar 5' },
      { src: require('@/assets/gallery/6.jpg'), description: 'tailbar 6' },
      { src: require('@/assets/gallery/7.jpg'), description: 'tailbar 7' },
      { src: require('@/assets/gallery/8.jpg'), description: 'tailbar 8' },
      { src: require('@/assets/gallery/9.jpg'), description: 'tailbar 9' },
      { src: require('@/assets/gallery/10.jpg'), description: 'tailbar 10' }
    ]
  }),
  mounted() {
    this.$store.commit('setTitle', this.title)
  },
  head: ({ title }) => ({ title })
}
</script>
