<template>
    <div class="ipad-mockup">
        <div class="story">
            <img src="../assets/img/visual-explanations/histoire.png" alt="Histoire" :style="style">
        </div>
        <img class="ipad" src="../assets/img/visual-explanations/mock_up_ipad.png" alt="iPad">
    </div>

</template>

<script>
    export default {
        name: 'i-pad-mockup',
        data () {
            return {
                ticking: false,
                lastScrollY: 0
            }
        },
        computed: {
            style () {
                return {
                    transform: `scale(1.5) translateX(-${this.lastScrollY}px)`
                }
            }
        },
        mounted() {
            this.observer = new IntersectionObserver(this.observeCallback.bind(this), {
                root: null,
                threshold: 0.2
            })
            this.observer.observe(this.$el)
            this.onScroll = this.onScroll.bind(this)
        },
        methods: {
            observeCallback(entries, observer) {
                entries.forEach(entry => {
                    if (entry.intersectionRatio > 0.2) {
                        window.addEventListener('scroll', this.onScroll)
                    } else {
                        window.removeEventListener('scroll', this.onScroll)
                    }
                })
            },
            onScroll () {
                this.lastScrollY = window.scrollY / 10
                if (!this.ticking) {
                    window.requestAnimationFrame(() => {
                        this.ticking = false;
                    })
                }
                this.ticking = true
            }
        }
    }
</script>

<style lang="scss">
    .ipad-mockup {
        width: 700px;
        margin: 0 auto;

        & img {
            width: 100%;

            &.ipad {
                z-index: 1;
                position: relative;
            }
        }
        & .story {
            position: absolute;
            z-index: 0;
            transform: translateX(100px);
            width: 500px;
            height: 529px;
            overflow: hidden;
            & img {
                position: absolute;
                top: 60px;
                width: 1400px;
                height: 278px;
                transform-origin: top left;
            }
        }
    }

</style>