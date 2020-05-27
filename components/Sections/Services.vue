<template>
  <div class="uk-section uk-section-default" uk-height-viewport>
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
      <div class="uk-child-width-1-2@m" uk-grid>
        <div v-for="(item, i) in items" :key="i">
          <div class="uk-flex-middle" uk-grid>
            <div
              class="uk-width-1-2 uk-text-center"
              :class="item.flip && 'uk-flex-last@m'"
            >
              <img :data-src="item.image" :alt="item.title" uk-img />
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
              <a
                href="#"
                class="uk-button uk-button-text"
                v-text="'- Learn More'"
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
    title: 'Our services',
    subtitle: 'To create a highly informed aimed society',
    items: [
      {
        title: 'Campaigns',
        image: require('@/assets/service1.jpg'),
        description:
          'The values of freedom, respect for human rights and the principle of holding periodic and genuine elections.'
      },
      {
        title: 'Elections',
        image: require('@/assets/service2.jpg'),
        description:
          'In its turn, democracy provides the natural environment for the protection and effective realization of human rights.'
      },
      {
        title: 'Our mission',
        image: require('@/assets/service3.jpg'),
        description:
          'We strengthen democratic institutions, support civil society and enhancing the law and judicial independence.',
        flip: true
      },
      {
        title: 'VOLUNTEERS',
        image: require('@/assets/service4.jpg'),
        description:
          'We seek to strengthen the legal framework and management practices to improve government response.',
        flip: true
      }
    ]
  })
}
</script>
