<script>
import ButtonComponent from './ButtonComponent.vue';
import PlayComponent from './PlayComponent.vue';
import SectionComponentShortcut from './MainSections/SectionComponentShortcut.vue';
import SectionComponentBattle from './MainSections/SectionComponentBattle.vue';
import SectionComponentFacts from './MainSections/SectionComponentFacts.vue';
import SectionComponentStreaming from './MainSections/SectionComponentStreaming.vue';


export default {
    name: 'PageMain',
    data() {
        return {


            blogArray: [
                {
                    path: 'img/blog-item-2.png',
                    title: 'Top 5 Most Important Aspects Of Your Game',
                },
                {
                    path: 'img/blog-item-3.png',
                    title: 'The Rise Of Fantasy Sports And Online Games',
                },
                {
                    path: 'img/blog-item-4.png',
                    title: 'Benefits Of Gaming - PC And Video Games',
                }
            ],
        }
    },
    components: {
        ButtonComponent,
        PlayComponent,
        SectionComponentShortcut,
        SectionComponentBattle,
        SectionComponentFacts,
        SectionComponentStreaming,
    },
    methods: {

    }
}
</script>

<template>
    <main class="my-0">

        <SectionComponentShortcut />

        <SectionComponentBattle />

        <SectionComponentFacts />

        <SectionComponentStreaming />




        <section class="bg-black feedback-section">
            <div class="container-xl">
                <div class="row justify-content-center text-center">
                    <div class="col-7">
                        <h4 class="my-green-text fw-bold">Futio Feedback</h4>
                        <h2 class="text-white fw-bold streaming-section-title py-2">
                            Watch Our Gamers Say
                        </h2>
                        <p class="text-light fw-light pb-5">
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor sit
                            ullam
                            placeat reiciendis
                            ducimus optio vel at corporis, omnis magni.
                        </p>
                    </div>
                </div>



            </div>
            <div class="discount-banner-bg">
                <div class="discount-banner-obj1">
                    <div class="discount-banner-obj2">
                        <div class="discount-banner text-center text-white py-5">
                            <h3>Make Offer</h3>
                            <h2 class="fw-bold">Get 70% Offer Discount</h2>
                            <button class="btn banner-button fw-bold text-white">
                                Get Offers
                            </button>
                        </div>
                    </div>

                </div>
            </div>

        </section>
        <section class="news-section bg-black">
            <div class="container-xl">
                <div class="row justify-content-center text-center">
                    <div class="col-7">
                        <h4 class="my-green-text fw-bold">Latest news</h4>
                        <h2 class="text-white fw-bold streaming-section-title py-2">
                            Stay Updated With Our Latest News Articles
                        </h2>
                        <p class="text-light fw-light pb-5">
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor sit
                            ullam
                            placeat reiciendis
                            ducimus optio vel at corporis, omnis magni.
                        </p>
                    </div>
                    <div class="col-6">
                        <div class="card rounded-5 blog-card">
                            <img class="card-img-top" src="img/blog-item-1.png" alt="Card image cap">
                            <div class="card-body">
                                <p class="text-start my-green-text">
                                    <span class="px-2">
                                        <img src="img/icon/clock.png" alt="">
                                    </span>
                                    10 min
                                    <span class="px-2">
                                        <img src="img/icon/eye.png" alt="">
                                    </span>
                                    240
                                    <span class="px-2">
                                        <img src="img/icon/calendar.png" alt="">
                                    </span>
                                    Apr 11, 2022
                                </p>
                                <h2 class="card-text text-white fw-bold text-start">
                                    Secrets To An Amazing Role Playing Game
                                </h2>
                            </div>
                        </div>
                    </div>
                    <div class="col-6">
                        <div>
                            <div v-for="(element, index) in blogArray" class="row blog-card rounded-5 mx-0 mb-2">
                                <div class="col-4">
                                    <img class="rounded-5" :src="element.path" alt="">
                                </div>
                                <div class="col-8 ps-5 pt-3">
                                    <p class="text-start my-green-text ">
                                        <span class="px-2">
                                            <img src="img/icon/clock.png" alt="">
                                        </span>
                                        10 min
                                        <span class="px-2">
                                            <img src="img/icon/eye.png" alt="">
                                        </span>
                                        240
                                        <span class="px-2">
                                            <img src="img/icon/calendar.png" alt="">
                                        </span>
                                        Apr 11, 2022
                                    </p>
                                    <h3 class="card-text text-white fw-bold text-start overflow-hidden">
                                        {{ element.title }}
                                    </h3>
                                </div>
                            </div>
                        </div>

                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use "../scss/variables.scss" as *;


.feedback-section {
    padding-top: 2%;


}

.news-section {
    padding-bottom: 10%;
}


.img-container {
    img {
        width: 100%;
    }
}


.discount-banner-bg {
    background-image: url(img/banner-item-bg.png);
    background-repeat: no-repeat;
    margin: auto;
    background-position: center;
    width: 1550px;
    height: 400px;



    .discount-banner-obj1 {
        background-image: url(img/banner-item-obj1.png);
        background-repeat: no-repeat;
        background-position-y: 4rem;
        height: 100%;



        .discount-banner-obj2 {
            background-image: url(img/banner-item-obj2.png);
            background-repeat: no-repeat;
            background-position-x: right;
            background-position-y: bottom;




            .discount-banner {
                h3 {
                    padding-top: 50px;
                }

                h2 {
                    padding-top: 20px;
                    padding-bottom: 20px;
                    font-size: 3.5em;
                }

            }
        }
    }
}

.banner-button {
    border-radius: 15% / 50%;
    padding-left: 50px;
    padding-right: 50px;
    padding-top: 20px;
    padding-bottom: 20px;
    background-color: $color-1;
}

.blog-card {
    background-color: $footer-bg-1;
}
</style>