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
      <div uk-filter="target: .js-filter">
        <div class="uk-grid-small uk-flex-middle" uk-grid>
          <div class="uk-width-expand">
            <ul class="uk-subnav uk-subnav-pill" uk-switcher>
              <li class="uk-active" uk-filter-control><a href="#">All</a></li>
              <li
                v-for="(tab, i) in tabs"
                :key="i"
                :uk-filter-control="`[data-tags*='${tab.key}']`"
              >
                <a href="#" v-text="tab.text" />
              </li>
            </ul>
          </div>
          <div class="uk-width-auto uk-text-nowrap">
            <span class="uk-active" uk-filter-control="sort: data-tags"
              ><a class="uk-icon-link" href="#" uk-icon="icon: arrow-down"></a
            ></span>
            <span uk-filter-control="sort: data-tags; order: desc"
              ><a class="uk-icon-link" href="#" uk-icon="icon: arrow-up"></a
            ></span>
          </div>
        </div>

        <ul class="js-filter uk-child-width-1-2 uk-child-width-1-3@m" uk-grid>
          <li
            v-for="(item, i) in items"
            :key="i"
            :data-tags="generateTags(item.tags)"
          >
            <div class="uk-card uk-background-muted">
              <div class="uk-card-body">
                <h3 class="uk-card-title" v-text="item.title" />
                <div class="uk-text-meta">
                  <span class="uk-text-primary" v-text="item.date" />
                </div>
                <p v-text="item.description" />
              </div>
              <div class="uk-card-media-bottom">
                <img :data-src="item.image" alt="" uk-img />
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
    title: "What's new?",
    subtitle: 'THE LATEST NEWS FROM THE CAMPAIGN',
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
        title: "WE SHOULD BE PROUD OF WHAT WE'VE ACHIEVED",
        description:
          'Maecenas Et Molestie Nibh. Cras Felis Leo, Tincidunt Quis Lorem...',
        image: require('@/assets/image1.jpg'),
        date: 'JULY 13, 2016',
        tags: [
          {
            text: 'Company News',
            key: 'company_news'
          }
        ]
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
