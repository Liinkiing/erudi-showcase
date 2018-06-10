<template>
  <div id="app">
    <presentation-component/>
    <footer-component/>
  </div>
</template>

<script>
import PresentationComponent from './components/Presentation-component'
import FooterComponent from './components/FooterComponent'

export default {
  name: 'app',
  components: {
    PresentationComponent,
    FooterComponent
  }
}
</script>

<style lang="scss">
  @import "assets/scss/app.scss";
</style>
