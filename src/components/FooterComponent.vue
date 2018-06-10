<template>
  <footer>
    <div class="container">
      <h3>Team érudi</h3>
      <div class="team-wrapper">
        <a :href="member.link" class="team-member" v-for="member in members">
          <img :src="member.img" alt="Avatar">
          <p>{{ member.first_name }}  {{ member.last_name }}</p>
        </a>
      </div>

      <div class="greetings">
        <h3>Remerciements</h3>
        <div class="greetings-text">
          <p>Nous remercions l’ensemble de l’équipe pédagogique de l’école des Gobelins pour leurs conseils et accompagnements qui a permis au projet Erudi de voir le jour !</p>

          <img src="./../assets/img/footer/greetings/gobelins_logo.png" alt="">
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import omarAvatar from './../assets/img/footer/team/omar.svg'
import sophieAvatar from './../assets/img/footer/team/sophie.svg'
import fanyAvatar from './../assets/img/footer/team/fany.svg'
import erwannAvatar from './../assets/img/footer/team/erwann.svg'

export default {
  name: 'footer-component',
  data () {
    return {
      members: [
        {
          link: 'https://github.com/Liinkiing',
          img: omarAvatar,
          first_name: 'Omar',
          last_name: 'Jbara',
          role: 'Développeur'
        },
        {
          link: 'http://sophielaplace.com/',
          img: sophieAvatar,
          first_name: 'Sophie',
          last_name: 'Laplace',
          role: 'Designer'
        },
        {
          link: '#',
          img: fanyAvatar,
          first_name: 'Fany',
          last_name: 'Thourain',
          role: 'Designer'
        },
        {
          link: 'https://github.com/Eronne',
          img: erwannAvatar,
          first_name: 'Erwann',
          last_name: 'Letue',
          role: 'Développeur'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "../assets/scss/colors";
  @import "../assets/scss/mixins";

  footer {
    padding: 6rem 0;
    text-align: center;
    color: $main-color;
    background-color: $footer-color;

    .team-wrapper {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      margin-top: 3rem;
      margin-bottom: 9rem;

      .team-member {
        width: calc((100% / 4) - 1rem);

        &:hover img {
          transform: scale(1.03);
        }

        @include tablet {
          width: 100%;
        }

        img {
          margin-bottom: 2rem;
          width: 19rem;
          transition: all .3s ease;
        }

        p {
          @include fontSize(22);
          font-family: tragic-marker, sans-serif;
          text-transform: uppercase;
        }
      }
    }

    .greetings {
      width: 100%;

      &-text {
        margin: 0 auto;
        margin-top: 4rem;
        max-width: 50rem;
      }

      img {
        margin-top: 3rem;
        width: 20rem;
      }
    }
  }
</style>
