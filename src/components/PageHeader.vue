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
            ]
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
            <div class="row">
                <div class="col">
                    <img id="logo" src="img/logo.png" alt="">
                </div>
                <div class="col-7 text-center">
                    <nav>
                        <ul class="text-white">
                            <li v-for="(navElement, index) in navMenu">
                                {{ navElement }} <img v-show="index > 0 && index < 5" src="img/svg/c-down-arrow.svg" alt="">
                            </li>
                        </ul>
                    </nav>
                </div>
                <div class="col-3">
                    <span class="shop-icon">
                        <img src="img/icon/cart-icon.png" alt="">
                        <span class="shop-counter">03</span>
                    </span>


                    <ButtonComponent />
                </div>
            </div>
        </div>

        <div class="banner-bg">
            <div class="container-xl">
                <div class="row my-0">
                    <div class="col-4 text-white">
                        <h2>Game With Live Streaming</h2>
                        <h1>Future of Esports</h1>
                        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Soluta beatae laboriosam minima
                            repellat?
                        </p>
                        <ButtonComponent /> <span>
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
    position: relative;
    z-index: -1;

    .banner-bg {
        background-image: url('./img/game-controler.png');
        background-repeat: no-repeat;
        background-position: left, bottom;
    }
}

nav {
    ul {
        li {
            display: inline;
            padding-right: 5px;

            img {
                display: inline;
            }
        }
    }
}

.shop-icon {
    position: relative;

    img {
        width: 30px;
    }


}

.shop-counter {
    font-size: 0.8rem;
    padding: 1px;
    border-radius: 50%/50%;
    color: black;
    background-color: $color-1;
    position: absolute;
    right: 1px;
    top: 1px;
}

.banner-image-container {
    width: 100%;

    .banner-image {
        width: 100%;
    }
}
</style>