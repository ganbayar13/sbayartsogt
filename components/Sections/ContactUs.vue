<template>
  <div class="uk-child-width-1-2" uk-grid>
    <div uk-height-viewport class="uk-background-primary">
      <GMap
        ref="gMap"
        language="en"
        :cluster="{ options: { styles: clusterStyle } }"
        :center="{ lat: locations[0].lat, lng: locations[0].lng }"
        :options="{ fullscreenControl: false, styles: mapStyle }"
        :zoom="6"
        height="100%"
      >
        <GMapMarker
          v-for="location in locations"
          :key="location.id"
          :position="{ lat: location.lat, lng: location.lng }"
          :options="{
            icon:
              location === currentLocation ? pins.selected : pins.notSelected
          }"
          @click="currentLocation = location"
        >
          <GMapInfoWindow>
            <code> lat: {{ location.lat }}, lng: {{ location.lng }} </code>
          </GMapInfoWindow>
        </GMapMarker>
        <GMapCircle :options="circleOptions" />
      </GMap>
    </div>
    <div class="uk-section uk-section-muted">
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
        <div class="uk-child-width-1-3@m" uk-grid>
          <div>
            <h5 class="uk-text-bold uk-text-uppercase" v-text="'Хаяг'" />
            <p class="uk-text-muted" v-text="'address here'" />
          </div>
          <div>
            <h5 class="uk-text-bold uk-text-uppercase" v-text="'Имэйл'" />
            <p class="uk-text-muted">
              <a href="mailto:name@example.com">
                name@example.com
              </a>
            </p>
          </div>
          <div>
            <h5 class="uk-text-bold uk-text-uppercase" v-text="'Утас'" />
            <p class="uk-text-muted" v-text="'+976 99111111'" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    title: 'Бидэндтэй холбогдох',
    subtitle: 'Таньд санал хүсэлт байвал имэйл бичнэ үү',
    currentLocation: {},
    circleOptions: {},
    locations: [
      {
        lat: 44.933076,
        lng: 15.629058
      },
      {
        lat: 45.815,
        lng: '15.9819'
      },
      {
        lat: '45.12',
        lng: '16.21'
      }
    ],
    pins: {
      selected: 'data:image/png;base64,iVBORw0KGgo...',
      notSelected: 'data:image/png;base64,iVBORw0KGgo...'
    },
    mapStyle: [],
    clusterStyle: [
      {
        url:
          'https://developers.google.com/maps/documentation/javascript/examples/markerclusterer/m1.png',
        width: 56,
        height: 56,
        textColor: '#fff'
      }
    ]
  })
}
</script>
