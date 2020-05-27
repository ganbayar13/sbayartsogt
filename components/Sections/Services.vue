<template>
  <div id="services" class="uk-section uk-section-default">
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
      <div class="uk-child-width-1-2@m uk-grid-match-height" uk-grid>
        <div v-for="(item, i) in items" :key="i">
          <div class="uk-flex-middle" uk-grid>
            <div
              class="uk-width-1-2 uk-text-center"
              :class="item.flip && 'uk-flex-last@m'"
            >
              <div class="uk-cover-container">
                <img :data-src="item.image" :alt="item.title" uk-img uk-cover />
                <canvas width="300" height="300" />
              </div>
            </div>
            <div class="uk-width-1-2">
              <h3 class="uk-text-uppercase">
                <span class="uk-text-muted" v-text="`0${i + 1}/`" />
                <span v-text="item.title" />
              </h3>
              <p
                class="uk-text-justify uk-text-muted"
                v-text="item.description"
              />
              <nuxt-link
                :to="item.to"
                class="uk-button uk-button-text"
                v-text="'Цааш унших'"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    title: 'Танилцуулга',
    subtitle:
      'ЭДИЙН ЗАСАГЧ, ХУУЛЬЧ МЭРГЭЖИЛТЭЙ, ОЛОН УЛСЫН ЭДИЙН ЗАСГИЙН УХААНЫ МАГИСТР',
    items: [
      {
        title: 'ТОВЧ НАМТАР',
        image: require('@/assets/service1.jpg'),
        to: '/namtar',
        description:
          'Сангажавын Баярцогт нь 1967 онд Сэлэнгэ аймгийн Сүхбаатар суманд төрсөн. 1984 онд Сэлэнгэ аймгийн Сүхбаатар хотын Г.Бумцэндийн нэрэмжит 10 жилийн 1 дүгээр дунд сургуулийг алтан медальтай төгссөн.'
      },
      {
        title: 'ЗУРГИЙН ЦОМОГ',
        image: require('@/assets/service2.jpg'),
        to: '/gallery',
        description:
          'Сангажавын Баярцогт нь сонгогч олныхоо итгэлийг хүлээн 1990 онд анхны ардчилсан чөлөөт сонгуулиар Ардын Их Хурлын депутат, Улсын Бага Хурлын гишүүнээр Сонгогдсоноос хойш нийтдээ Монгол Улсын хууль тогтоох байгууллагад 5 удаа сонгогдон ажилласан зургуудаас.'
      }
    ]
  })
}
</script>
