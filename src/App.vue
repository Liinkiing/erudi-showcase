<template>
  <div id="app">
    <presentation-component/>
    <demonstration-component/>
    <footer-component/>
  </div>
</template>

<script>
import PresentationComponent from './components/Presentation-component'
import DemonstrationComponent from './components/DemonstrationComponent'
import FooterComponent from './components/FooterComponent'

export default {
  name: 'app',
  components: {
    PresentationComponent,
    DemonstrationComponent,
    FooterComponent
  }
}
</script>

<style lang="scss">
  @import "assets/scss/app.scss";
</style>
