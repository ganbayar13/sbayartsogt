<template>
  <div class="uk-child-width-1-2@m uk-grid-collapse" uk-grid uk-height-viewport>
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
        <h4 v-text="'THE IMPORTANT ISSUES OUR NATION FACES'" />
        <div
          class="uk-grid-small uk-child-width-1-2 uk-width-xlarge@m"
          uk-grid
          uk-margin
        >
          <div
            v-for="(item, i) in items"
            :key="i"
            class="uk-text-primary uk-text-uppercase uk-text-small"
          >
            {{ item }}
          </div>
        </div>
        <a
          class="uk-button uk-button-primary uk-margin-large-top"
          v-text="'Learn More'"
        />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    title: 'JOIN US, AND LET’S GET TO WORK',
    description:
      'How can we get our country back on track? How to preserve our Constitution and get people value and honor it? All this core questions have been evolving in our minds for years. And now we have all the answers to them. Join us and change your future.',
    items: [
      'ENTITLEMENT REFORM',
      'CRIMINAL JUSTICE REFORM',
      'FOREIGN POLICY',
      'THE ECONOMY',
      'EDUCATION',
      'VETERAN HEALTHCARE'
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
