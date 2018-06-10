<template>
    <div class="presentation">
        <div class="container">
            <div class="presentation-logo">
                <img src="./../assets/img/presentation/erudi-logo.png" alt="Logo">

                <div class="presentation-text pitch">
                    <h2>Le pitch</h2>
                    <p>Erudi est un voyage interactif sensoriel qui permet aux enfants âgés entre 6 et 9 ans de s’ouvrir aux différentes cultures du monde </p>
                </div>
            </div>

            <div class="presentation-text concept">
                <h2>Le concept</h2>
                <p>Un tour du monde culturel immersif faisant appel aux 5 sens par le biais des contes populaires</p>
            </div>

            <div class="presentation-text kit">
                <h2>Le dispositif</h2>
                <p>Un coffret physique et numérique, idéal pour une immersion totale</p>
            </div>

            <div class="presentation-kit">
                <div class="presentation-kit__item">
                    <img src="./../assets/img/presentation/kit/ipad.png" alt="Ipad">
                    <p>Une application interactive</p>
                </div>

                <div class="presentation-kit__item">
                    <img src="./../assets/img/presentation/kit/totem.png" alt="Totem">
                    <p>Diffuseur d'odeurs</p>
                </div>

                <div class="presentation-kit__item">
                    <img src="./../assets/img/presentation/kit/caps.png" alt="Capsules d'odeurs">
                    <p>Des capsules d'odeurs</p>
                </div>

                <div class="presentation-kit__item">
                    <img src="./../assets/img/presentation/kit/book.png" alt="Carnet d'odeurs">
                    <p>Un carnet d'odeurs</p>
                </div>

                <div class="presentation-kit__item">
                    <img src="./../assets/img/presentation/kit/map.png" alt="Carte du monde">
                    <p>Une carte du monde papier</p>
                </div>
            </div>

            <div class="presentation-video">
                <h2>Teaser</h2>
                <div class="presentation-video__iframe">
                    <!-- Todo: Add iframe -->
                </div>
            </div>
        </div>

        <div class="presentation-worldmap">
            <div class="presentation-text worldmap">
                <h2>Une carte interactive</h2>
                <p>Déplace toi sur la carte et choisi ta prochaine destination !</p>
            </div>
            <img src="../assets/img/presentation/worldmap.png" alt="WorldMap">
        </div>
    </div>
</template>

<script>
export default {
    name: 'presentation-component'
}
</script>

<style lang="scss" scoped>
    @import "./../assets/scss/colors";
    @import "./../assets/scss/mixins";

	.presentation {
        min-height: 100vh;

        &::before {
            z-index: -1;
            content: url("./../assets/img/presentation/presentation_bg.svg");
            position: absolute;
            width: 100vw;
        }

        &-logo {
            margin-bottom: 18rem;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            text-align: center;
            flex-direction: column;

            &::after {
                content: url("./../assets/img/presentation/plane.png");
                position: absolute;
                top: 30rem;
                left: 50%;
                transform: translateX(-50%);
            }

            img {
                width: 100%;
            }
        }

        &-text {
            margin: 0 auto;
            max-width: 40rem;
            text-align: center;

            h2 {
                margin-bottom: 2rem;
            }

            &.pitch {
                margin-top: 6rem;
            }

            &.concept{
                margin-bottom: 8rem;
            }

            &.kit {
                margin-bottom: 8rem;
            }

            &.worldmap {
                position: absolute;
                bottom: 10rem;
                right: 10rem;
                text-align: left;
            }
        }

        &-kit {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: flex-start;

            &__item {
                display: flex;
                justify-content: space-between;
                align-items: center;
                flex-direction: column;
                width: calc((100% / 5) -1rem);
                height: 17rem;
                text-align: center;

                @include tablet {
                    width: 100%;
                }

                p {
                    max-width: 70%  ;
                }
            }
        }

        &-video  {
            text-align: center;

            h2 {
                margin-bottom: 4rem;
            }

            &__iframe {
                margin: 0 auto;
                width: 64rem;
                height: 36rem;
                background-color: $main-color;
            }
        }

        &-worldmap {
            position: relative;

            img {
                width: 100%;
            }
        }
    }
</style>