<template>
  <div class="demonstration">
    <div class="container">
      <h2>Démonstration</h2>

      <div class="demonstration-iframe iframe">
        <iframe src="https://player.vimeo.com/video/274980795" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
      </div>
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
    & h2 {
      padding-top: 40px;
    }

    &-iframe {
      position: relative;
      margin-top: 8rem;
      width: 100%;
      height: 64rem;
      & iframe {
        width: 100%;
      }
      &::after {
        content: url("../assets/img/demonstration/mountains.png");
        position: absolute;
        top: -1px;
        right: 1.5rem;
        transform: translateY(-98%);
      }
    }

    img {
      display: block;
    }
  }
</style>
