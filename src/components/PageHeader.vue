<script>
import ButtonComponent from './ButtonComponent.vue';
import PlayComponent from './PlayComponent.vue';

export default {
    name: 'PageHeader',
    data() {
        return {
            navMenu: [
                'Home',
                'Games',
                'Shop',
                'Pages',
                'Blog',
                'Contact'
            ],
        }
    },
    components: {
        ButtonComponent,
        PlayComponent,
    },
    methods: {

    }
}
</script>

<template>
    <header class="my-header-bg my-0">
        <div class="container-xl">
            <div class="row py-5">
                <div class="col">
                    <img id="logo" src="img/logo.png" alt="">
                </div>
                <div class="col-7 text-center">
                    <nav>
                        <ul class="fs-5">
                            <li v-for="(navElement, index) in navMenu">

                                <a class="nav-links px-2" href="">{{ navElement }} <img v-show="index > 0 && index < 5"
                                        src="img/svg/c-down-arrow.svg" alt="">
                                </a>

                            </li>
                        </ul>
                    </nav>
                </div>
                <div class="col-3">
                    <span class="shop-icon">
                        <img src="img/icon/cart-icon.png" alt="">
                        <span class="shop-counter">03</span>
                    </span>


                    <ButtonComponent buttonText="LIVE STREAMING" />
                </div>
            </div>
        </div>

        <div class="banner-bg">
            <div class="container-xl">
                <div class="row">
                    <div class="col-4 text-white my-header-content">
                        <h4 class="my-green-text fw-bold">Game With Live Streaming</h4>
                        <h1>Future of Esports</h1>
                        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Soluta beatae laboriosam minima
                            repellat?
                        </p>
                        <ButtonComponent buttonText="EXPLORE GAMES" />
                        <span class="play-from-header">
                            <PlayComponent />
                        </span>
                    </div>
                    <div class="col-8">
                        <div class="banner-image-container">
                            <img class="banner-image" src="img/index-banner-illus.png" alt="">
                        </div>

                    </div>
                </div>
            </div>
        </div>

    </header>
</template>

<style lang="scss" scoped>
@use "../scss/variables.scss" as *;

.my-header-bg {
    background-image: url('./img/index-banner-bg.png');
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
    z-index: -1;

    .banner-bg {
        background-image: url('./img/game-controler.png');
        background-repeat: no-repeat;
        background-position-x: left;
        background-position-y: bottom;
    }
}

.my-header-content {
    padding-top: 10%;

    h1 {
        font-size: 4.2em;
        font-weight: bold;
    }
}

nav {
    ul {

        li {
            padding-right: 5px;
            display: inline;

            img {
                display: inline;
            }
        }
    }
}

.nav-links:hover {
    color: $color-2;
}

.play-from-header {
    padding-left: 15px;
}

.shop-icon {
    position: relative;
    padding-right: 15px;

    img {
        width: 35px;
    }


}

.shop-counter {
    font-size: 0.8rem;
    padding: 1px;
    border-radius: 50%/50%;
    color: black;
    background-color: $color-1;
    position: absolute;
    left: 1rem;
    bottom: 0.5rem;
}

.banner-image-container {
    width: 100%;

    .banner-image {
        width: 100%;

    }
}
</style>