<template>
  <div id="app">
    <presentation-component/>
    <visual-explanations/>
    <demonstration-component/>
    <footer-component/>
  </div>
</template>

<script>
import PresentationComponent from './components/PresentationComponent'
import VisualExplanations from './components/VisualExplanations'
import DemonstrationComponent from './components/DemonstrationComponent'
import FooterComponent from './components/FooterComponent'

export default {
  name: 'app',
  components: {
    PresentationComponent,
    VisualExplanations,
    DemonstrationComponent,
    FooterComponent
  }
}
</script>

<style lang="scss">
  @import "assets/scss/app.scss";
</style>
