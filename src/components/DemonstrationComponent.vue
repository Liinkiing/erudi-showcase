<template>
  <div class="demonstration">
    <div class="container">
      <h2>Démonstration</h2>

      <div class="demonstration-iframe iframe"></div>
    </div>

    <img src="../assets/img/demonstration/illustration.svg" alt="Illustration">
  </div>
</template>

<script>
export default {
  name: 'demonstration-component'
}
</script>

<style lang="scss" scoped>
  @import "../assets/scss/colors";
  @import "../assets/scss/mixins";

  .demonstration {
    text-align: center;
    background-color: $sky-color;

    &-iframe {
      position: relative;
      margin-top: 8rem;

      &::after {
        content: url("../assets/img/demonstration/mountains.png");
        position: absolute;
        top: 0;
        right: -.6rem;
        transform: translateY(-98%);
      }
    }

    img {
      display: block;
    }
  }
</style>
