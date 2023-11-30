<template>
  <div v-if="feature" class="popup">
    <h3>{{ feature.properties.title }}</h3>
    <p>{{ feature.properties.description }}</p>
  </div>
</template>

<script>
export default {
  name: 'Popup',
  props: {
    feature: Object
  }
};
</script>

<style scoped>
.popup {
  position: absolute;
  z-index: 10;
  background: white;
  padding: 10px;
  border: 1px solid #ccc;
}
</style>
