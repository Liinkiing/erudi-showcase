<template>
    <div class="presentation">
        <div class="presentation-logo">
            <div class="container">
                <img src="./../assets/img/presentation/erudi-logo.png" alt="Logo">

                <img class="plane" src="./../assets/img/presentation/plane.png" alt="Plane">

                <div class="text-group pitch">
                    <h2>Le pitch</h2>
                    <p>Erudi est un voyage interactif sensoriel qui permet aux enfants âgés entre 6 et 9 ans de s’ouvrir aux différentes cultures du monde </p>
                </div>
            </div>
        </div>

        <div class="presentation-content">
            <div class="container">
                <div class="text-group concept">
                    <h2>Le concept</h2>
                    <p>Un tour du monde culturel immersif faisant appel aux 5 sens par le biais des contes populaires</p>
                </div>

                <div class="text-group kit">
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
                    <div class="iframe">
                        <iframe src="https://player.vimeo.com/video/274977095" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
                    </div>
                </div>
            </div>
        </div>

        <div class="presentation-worldmap">
            <div class="text-group worldmap">
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
        background-color: $sky-color;
        &-logo {
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 80vh;
            text-align: center;
            flex-direction: column;
            background-color: $bg-logo-color;

            @include tablet {
                height: 80vh;
            }

            .plane {
                z-index: 2;
                position: absolute;
                top: 27rem;
                left: 50%;
                transform: translateX(-50%);
                width: 45%;

                @include tablet {
                    top: 33rem;
                    width: 70%;
                }

                @include mobile {
                    top: 35rem;
                    width: 90%;
                }
            }

            &::after {
                z-index: 1;
                content: url("./../assets/img/presentation/presentation-shape.svg");
                position: absolute;
                top: 75vh;
                left: 0;
                width: 100%;

                @include tablet {
                    top: 80vh;
                }
            }

            img {
                width: 100%;
            }
        }

        &-content {
            padding-top: 38rem;

            @include tablet {
                padding-top: 24rem;
            }
        }

        .text-group {
            &.pitch {
                z-index: 2;
                position: absolute;
                bottom: -8rem;
                left: 50%;
                transform: translateX(-50%);
                margin-top: 4rem;

                @include tablet {
                    bottom: 5%;
                }
            }

            &.concept{
                margin-bottom: 10rem;
            }

            &.kit {
                margin-bottom: 8rem;
            }

            &.worldmap {
                position: absolute;
                bottom: 10rem;
                right: 10rem;
                text-align: left;

                @include tablet {
                    margin-top: 15rem;
                    margin-bottom: 6rem;
                    position: static;
                    text-align: center;
                }
            }
        }

        &-kit {
            margin-bottom: 15rem;
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
                    height: 14rem;
                    margin-top: 6rem;

                    &:first-of-type {
                        margin-top: 0;
                    }
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
        }

        &-worldmap {
            position: relative;
            margin-top: 4rem;

            img {
                margin-left: -2.5%;
                width: 105%;
            }
        }
    }
</style>