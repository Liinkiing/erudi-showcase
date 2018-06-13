<template>
  <div class="visual-explanations">
    <div class="container">
      <div class="text-group">
        <h2>Une histoire immersive</h2>
        <p>Découvre le pays à travers un conte populaire interactif qui met à l’honneur les sens avec : le son, le touché et l’odorat !</p>
      </div>
      <i-pad-mockup/>
      <div class="text-group">
        <p>A chaque pays sa senteur. Pendant la lecture garde pres de toi ton diffuseur. Il te fera voyager en propageant une odeur.</p>
      </div>

      <div class="row">
        <div class="text-group">
          <h2>Un carnet d'exploration</h2>
          <p>Dans ton carnet d’exploration tu observera ton évolution !</p>
        </div>
        <img src="../assets/img/visual-explanations/carnet.png" alt="Carnet d'exploration">
      </div>

      <div class="row inversed">
        <div class="text-group">
          <h2>Une fiche informative</h2>
          <p>Approfondi tes connaissances sur les pays visités. Découvre sa faune et sa flore !</p>
        </div>
        <img src="../assets/img/visual-explanations/fiche.png" alt="Informations pays">
      </div>

      <div class="row">
        <div class="text-group">
          <h2>Une fiche recette</h2>
          <p>Découvre le goût de l’odeur à travers une recette typique du pays choisi.</p>
        </div>
        <img src="../assets/img/visual-explanations/recette.png" alt="Informations recettes">
      </div>


    </div>
  </div>
</template>

<script>

import IPadMockup from "./iPadMockup";

export default {
    components: {IPadMockup},
    name: 'visual-explanations'
}
</script>

<style lang="scss" scoped>
  @import "../assets/scss/colors";
  @import "../assets/scss/mixins";

  .visual-explanations {
    background-color: $visual-color;
    padding: 60px;
    .row {
      margin: 40px 0;
      display: flex;
      align-items: center;
      &.inversed {
        flex-direction: row-reverse;
      }

      img {
        width: 729px;
      }
    }
    .row, .row.inversed {
      @include tablet {
        flex-direction: column;
        justify-content: center;
        text-align: center;
      }
    }
    .text-group {
      text-align: left;
    }

  }
</style>
