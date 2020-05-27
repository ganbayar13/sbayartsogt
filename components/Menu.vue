<template>
  <div
    class="sidebar uk-flex uk-flex-column uk-flex-between uk-flex-middle"
    uk-sticky
    uk-height-viewport
  >
    <div>
      <a
        class="uk-navbar-toggle"
        uk-navbar-toggle-icon
        uk-toggle
        href="#offcanvas"
      />
    </div>
    <div>
      <div class="rotate uk-text-uppercase">
        <ul
          class="uk-nav title uk-animation-fast"
          uk-scrollspy-nav="cls: uk-animation-fade uk-active; closest: li; overflow: false; offset: 200"
        >
          <li v-for="(item, i) in items" :key="i">
            <a class="uk-disabled" :href="item.anchor" v-text="item.text" />
          </li>
        </ul>
      </div>
    </div>
    <div>
      <ul
        class="uk-nav numbers uk-nav-default uk-light"
        uk-scrollspy-nav="closest: li; scroll: true; cls: invert; overflow: false; offset: 200"
      >
        <li v-for="(item, i) in items" :key="i">
          <a :href="item.anchor" class="uk-text-center">
            <span v-text="i + 1" />
            <i uk-icon="icon: minus" />
          </a>
        </li>
      </ul>
    </div>
    <div class="uk-margin">
      <a href="#" uk-totop uk-scroll></a>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    items: [
      {
        text: 'Эхлэл',
        anchor: '#start'
      },
      {
        text: 'Танилцуулга',
        anchor: '#services'
      },
      {
        text: 'Бидний тухай',
        anchor: '#about'
      },
      {
        text: 'Мэдээ мэдээлэл',
        anchor: '#news'
      },
      {
        text: 'Сонин сэтгүүл',
        anchor: '#magazine'
      },

      {
        text: 'Он цагийн хэлхээ',
        anchor: '#timeline'
      },
      {
        text: 'Холбоо барих',
        anchor: '#contactus'
      }
    ]
  })
}
</script>
<style>
.rotate {
  transform: rotate(-90deg);
  -webkit-transform: rotate(-90deg);
  -moz-transform: rotate(-90deg);
  -ms-transform: rotate(-90deg);
  -o-transform: rotate(-90deg);
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
}
ul.uk-nav.title {
  width: 200px;
}
ul.uk-nav.title li {
  display: none;
}
ul.uk-nav.title li a {
  color: #ffffff;
  text-decoration: none;
}
ul.uk-nav.title li.uk-active {
  display: block;
}
ul.uk-nav li a {
  color: #ffffff !important;
}
ul.uk-nav li a span {
  display: none;
  font-weight: bold;
}
ul.uk-nav li a i {
  display: block;
}
li.invert i,
li.uk-nav:hover a i {
  display: none !important;
}
li.invert span,
li.uk-nav:hover a span {
  display: block !important;
}
</style>
