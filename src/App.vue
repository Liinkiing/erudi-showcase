<template>
  <div id="app">
    <footer-component/>
  </div>
</template>

<script>
import FooterComponent from './components/FooterComponent.vue'

export default {
  name: 'app',
  components: {
    FooterComponent
  }
}
</script>

<style lang="scss">
  @import "assets/scss/app.scss";
</style>
