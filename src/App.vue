<template>
  <div id="map" />
</template>

<script>
// Import mapbox
import mapboxgl from "mapbox-gl";
import "mapbox-gl/dist/mapbox-gl.css";
import { onMounted } from "vue";


export default {

  setup() {
    onMounted(() => {
      // You can get you access token from https://account.mapbox.com/
      mapboxgl.accessToken =
        "ACCESS TOKEN";
      const map = new mapboxgl.Map({
        container: "map",
        center: [69.17535264597393,34.51983332233756],
        zoom: 18,
        // You can create a new style in mapbox studio and enable the 3d building and than insert the you style link here
        style: "YOUR CUSTOMIZED STYLE FROM https://studio.mapbox.com/",
        // Pitch means the angel of map view which you need in 3d building mode
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