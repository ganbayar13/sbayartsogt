<template>
  <div id="news" class="uk-section uk-section-default" uk-height-viewport>
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
      <div>
        <ul class="js-filter uk-child-width-1-2 uk-child-width-1-3@m" uk-grid>
          <li v-for="(item, i) in items" :key="i">
            <div class="uk-card uk-background-muted">
              <div class="uk-card-body">
                <h3
                  class="uk-card-title uk-text-uppercase uk-margin-remove-bottom"
                  v-text="item.title"
                />
                <div class="uk-text-meta">
                  <span class="uk-text-primary" v-text="item.date" />
                </div>
                <p v-text="item.description" />
              </div>
              <div class="uk-card-media-bottom">
                <img :src="item.image" alt="" />
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    title: 'Мэдээ мэдээлэл',
    subtitle: 'НЭР ДЭВШИГЧИЙН ХАМГИЙН СҮҮЛИЙН ҮЕИЙН МЭДЭЭ МЭДЭЭЛЛИЙГ ТАНД',
    tabs: [
      {
        text: 'Company News',
        key: 'company_news'
      },
      {
        text: 'General News',
        key: 'general_news'
      },
      {
        text: 'Economics',
        key: 'economics'
      }
    ],
    items: [
      {
        title: '4000 хүн ам тутамд гал түймэр унтраах аврах анги байх ёстой',
        description:
          'Хүний амьдралд асар том хохирол, хор уршиг авчирдаг аюул бол гал түймэр. Хүн ам олширч, барилга байшин нэмэгдэхийн хэрээр гал түймэр гарах эрсдэл нэмэгдэж байдаг...',
        image: require('@/assets/image1.jpg'),
        date: '3-р сар 13, 2020'
      },
      {
        title: '4000 хүн ам тутамд гал түймэр унтраах аврах анги байх ёстой',
        description:
          'Хүний амьдралд асар том хохирол, хор уршиг авчирдаг аюул бол гал түймэр. Хүн ам олширч, барилга байшин нэмэгдэхийн хэрээр гал түймэр гарах эрсдэл нэмэгдэж байдаг...',
        image: require('@/assets/image1.jpg'),
        date: '3-р сар 13, 2020'
      },
      {
        title: '4000 хүн ам тутамд гал түймэр унтраах аврах анги байх ёстой',
        description:
          'Хүний амьдралд асар том хохирол, хор уршиг авчирдаг аюул бол гал түймэр. Хүн ам олширч, барилга байшин нэмэгдэхийн хэрээр гал түймэр гарах эрсдэл нэмэгдэж байдаг...',
        image: require('@/assets/image1.jpg'),
        date: '3-р сар 13, 2020'
      }
    ]
  }),
  methods: {
    generateTags(tags) {
      if (tags && tags.length > 0) {
        const keys = []
        tags.map((tag) => {
          keys.push(tag.key)
        })
        return keys
      }
      return null
    }
  }
}
</script>
