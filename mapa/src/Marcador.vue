<template>
    <div></div>
  </template>
  
  <script>
  export default {
    name: 'Marcador',
    props: {
      feature: Object
    },
    mounted() {
      const { coordinates } = this.feature.geometry;
  
      new mapboxgl.Marker()
        .setLngLat(coordinates)
        .addTo(this.$parent.map);
    }
  };
  </script>
  