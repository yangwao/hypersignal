<template>
  <div>
    <div id="map-inner" style="height: 80%">
        {{ center.lat }}, {{ center.lng }}
      </br>
      <v-map style="height: 40%" :zoom="zoom" :center="center">
        <v-tilelayer :url="url" :attribution="attribution"></v-tilelayer>
        <v-circle :lat-lng="circle.center" :radius="circle.radius"></v-circle>
      </v-map>
    </div>
  </div>
</template>

<script>
import Vue2Leaflet from 'vue2-leaflet';

export default {
  name: 'simple',
  components: {
    'v-map': Vue2Leaflet.Map,
    'v-tilelayer' :Vue2Leaflet.TileLayer,
    'v-circle': Vue2Leaflet.LCircle
  },
  data () {
    return {
      zoom:11,
      center: L.latLng(48.1389601,17.0878431),
      url:'http://{s}.tile.osm.org/{z}/{x}/{y}.png',
      attribution:'&copy; <a href="http://osm.org/copyright">OpenStreetMap</a> contributors',
      circle: {
        center: L.latLng(48.1389601,17.0878431),
        radius: 5000
      }
    }
  }
}
</script>

<style>
@import "~leaflet/dist/leaflet.css";
</style>
