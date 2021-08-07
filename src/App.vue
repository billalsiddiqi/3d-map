<template>
  <div id="map" />
</template>

<script>

import mapboxgl from "mapbox-gl";
import "mapbox-gl/dist/mapbox-gl.css";
import { onMounted } from "vue";
export default {
  setup() {
    onMounted(() => {
      mapboxgl.accessToken =
        "pk.eyJ1IjoiY2FwaTIwNzciLCJhIjoiY2tzMWRvYW5sMXQzZDJwczd4bHk0OGptdSJ9.3tahM0wZbCq3nYrnnxPL8A";
      const map = new mapboxgl.Map({
        container: "map",
        center: [69.17535264597393,34.51983332233756],
        zoom: 18,
        style: "mapbox://styles/capi2077/cks1kfmir1mrg18o47sstus7e",
        pitch: 60,
      });
      map.on('load', () => {
         
      });
    });
    return {};
  },
};
</script>

<style>
#map {
  height: 100vh;
}
</style>