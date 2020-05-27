<template>
  <div id="magazine" class="uk-section uk-section-muted" uk-height-viewport>
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
        <div>
          <iframe
            src="http://online.fliphtml5.com/cauwv/ivcl/?fbclid=IwAR0QGsYj0bltlnbMZtdbtaWXkruYjn-WBqwohaZhPpS4yaO9s0LN6HhvOac"
            class="uk-responsive-width"
            width="1024"
            height="728"
            uk-responsive
          />
        </div>
        <div>
          <iframe
            src="http://online.fliphtml5.com/cauwv/ivcl/?fbclid=IwAR0QGsYj0bltlnbMZtdbtaWXkruYjn-WBqwohaZhPpS4yaO9s0LN6HhvOac"
            class="uk-responsive-width"
            width="1024"
            height="728"
            uk-responsive
          />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    title: 'Сонин, Сэтгүүл',
    subtitle: 'Цахимаар сонин сэтгүүлийг уншиж танилцана уу'
  })
}
</script>
