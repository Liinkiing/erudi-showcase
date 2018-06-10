<template>
  <footer>
    <div class="container">
      <h3>Team érudi</h3>
      <div class="team-wrapper">
        <div class="team-member" v-for="member in 4">
          <p>Name</p>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'footer-component'
}
</script>

<style lang="scss" scoped>
  @import "../assets/scss/colors";
  @import "../assets/scss/mixins";

  footer {
    text-align: center;
    color: $main-color;
    background-color: $footer-color;

    h3 {
      font-family: tragic-marker, sans-serif;
    }

    .team-wrapper {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      margin-top: 3rem;

      .team-member {
        width: calc((100% / 4) - 1rem);

        @include tablet {
          width: 100%;
        }
      }
    }
  }
</style>
