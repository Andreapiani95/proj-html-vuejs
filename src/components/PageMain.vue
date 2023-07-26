<script>
import ButtonComponent from './ButtonComponent.vue';
import PlayComponent from './PlayComponent.vue';
export default {
    name: 'PageMain',
    data() {
        return {
            shortcutSection: [
                {
                    title: 'Live Streaming',
                    path: 'img/icon/features-icon-1.png'
                },
                {
                    title: 'Great Tournament',
                    path: 'img/icon/features-icon-2.png'
                },
                {
                    title: 'Gaming News',
                    path: 'img/icon/features-icon-3.png'
                },
            ],

            battleSection: [
                {
                    team1: 'img/game-img-1.png',
                    team2: 'img/game-img-2.png',
                    title: 'Call of Deauty',
                },
                {
                    team1: 'img/game-img-3.png',
                    team2: 'img/game-img-4.png',
                    title: 'Legendary Battles',
                },
                {
                    team1: 'img/game-img-5.png',
                    team2: 'img/game-img-6.png',
                    title: 'Nay Corral Gundown',
                },
                {
                    team1: 'img/game-img-7.png',
                    team2: 'img/game-img-8.png',
                    title: 'League Of Legends',
                },
            ],

            quickFacts: [
                {
                    number: '1135',
                    title: 'Twitch Streams',
                },
                {
                    number: '44',
                    title: 'Total games',
                },
                {
                    number: '982',
                    title: 'Youtube Streams',
                },
                {
                    number: '40',
                    title: 'Pro Teams',
                },
            ],

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
    },
    methods: {

    }
}
</script>

<template>
    <main class="my-0">
        <section class="bg-black">
            <div class="main-section-1">
                <div class="row">
                    <div class="col-6">
                        <div class="img-container">
                            <img src="img/features-illus.png" alt="">
                        </div>
                    </div>
                    <div class="col-4 text-white">
                        <h4 class="my-green-text fw-bold">The Ultimate Competitive Gaming Platform</h4>
                        <h2 class="fw-bold main-section-1-title">Make Your Own Mark On The Battle Field</h2>
                        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Consectetur, exercitationem perferendis
                            nihil quibusdam optio vitae voluptatibus debitis ipsam, enim rerum facere nam reiciendis dolore
                            aliquam ex in laboriosam quasi repellat!
                        </p>
                        <div class="pb-5">
                            <div v-for="(element, index) in  shortcutSection " class="row">
                                <div class="col-3">
                                    <img :src="element.path" alt="  ">
                                </div>
                                <div class="col-9">
                                    <h4 class="pb-2">{{ element.title }}</h4>
                                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque cum pariatur
                                        aspernatur commodi quia? Doloremque?</p>
                                </div>
                            </div>
                        </div>
                        <ButtonComponent buttonText="PLAN NOW" />
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-battle">
            <div class="container-xl">
                <div class="row justify-content-center text-center">
                    <div class="col-7">
                        <h4 class="my-green-text fw-bold">Trending Battle</h4>
                        <h2 class="text-white fw-bold battle-section-title py-2">
                            Keep Eyes & Manage Upcoming Battle
                        </h2>
                        <p class="text-light fw-light pb-5">
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor sit
                            ullam
                            placeat reiciendis
                            ducimus optio vel at corporis, omnis magni.
                        </p>
                    </div>
                </div>
                <div class="row">
                    <div v-for="(element, index) in battleSection" class="col-6">
                        <div class="card my-card-battle rounded-4 my-3">
                            <div class="row justify-content-between py-3">
                                <div class="col-4 battle-icon">
                                    <img :src="element.team1" alt="">
                                </div>
                                <div class="col-4 battle-icon">
                                    <img class="versus-icon" src="img/versus-icon.png" alt="">
                                </div>
                                <div class="col-4 battle-icon">
                                    <img :src="element.team2" alt="">
                                </div>
                            </div>
                            <div class="card-body text-center my-card-body">
                                <p class="card-text">
                                <h3 class="text-white py-3">{{ element.title }}</h3>
                                <p class="my-green-text">December 25, 2022 4:00 PM</p>
                                </p>
                            </div>
                            <div class="card-body row justify-content-center text-white">
                                <div class="col-5">
                                    <span>
                                        <img src="img/icon/youtube-icon.png" alt="">
                                    </span>
                                    <span class="pe-2">
                                        Youtube
                                    </span>
                                    <span>
                                        <img src="img/icon/twitch-icon.png" alt="">
                                    </span>
                                    <span>
                                        Twitch
                                    </span>
                                </div>

                            </div>
                        </div>
                    </div>
                </div>
                <div class="text-center pt-5">
                    <ButtonComponent buttonText="VIEW ALL MATCH" />
                </div>

            </div>
        </section>

        <section class="bg-black quick-facts-section">
            <div class="container-xl">
                <h2 class="text-center text-white fw-bold">Futio Quick Facts</h2>
                <div class="row">
                    <div class="col-3" v-for="(element, index) in quickFacts">
                        <div class="card bg-transparent border rounded-5">
                            <div class="card-body text-center">
                                <h2 class="text-white">{{ element.number }}</h2>
                                <p class="my-green-text">{{ element.title }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <section class="streaming-section">
            <div class="container-xl">
                <div class="row justify-content-center text-center">
                    <div class="col-7">
                        <h4 class="my-green-text fw-bold">Live Streaming</h4>
                        <h2 class="text-white fw-bold streaming-section-title py-2">
                            Watch The Streams
                        </h2>
                        <p class="text-light fw-light pb-5">
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor sit
                            ullam
                            placeat reiciendis
                            ducimus optio vel at corporis, omnis magni.
                        </p>
                    </div>
                    <div class="col-9 card my-streaming-card rounded-5">
                        <img src="img/stream-bg-3.png" alt="">

                        <div class="live-icon ">
                            <div class="rounded-5">
                                <img src="img/icon/live-icon.png" alt="">
                                <span>Live</span>
                            </div>

                        </div>


                        <div class="live-play">
                            <PlayComponent />
                            <h4 class="text-white fw-bold">
                                League of Legends
                            </h4>
                        </div>


                        <div class="live-counter">
                            <span class="my-green-text">
                                356.599
                            </span>
                            <span class="text-white">
                                Viewers
                            </span>
                            <span class="my-green-text">
                                23.599
                            </span>
                            <span class="text-white">
                                Likes
                            </span>
                        </div>


                    </div>

                </div>
            </div>


        </section>
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
                                    <h3 class="card-text text-white fw-bold text-start">
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


.main-section-1 {
    padding-top: 7%;
    padding-bottom: 7%;
}

.main-section-1-title {
    font-size: 3rem;
}

.battle-section-title,
.streaming-section-title {
    font-size: 3.5rem;
}

.quick-facts-section {
    padding-top: 5%;
    padding-bottom: 5%;

    div {
        h2 {
            font-size: 3.5em;
            padding-bottom: 5%;
        }
    }
}

.streaming-section {
    width: 100%;
    background-color: black;
    background-image: url('img/live-streaming-bg.png');
    background-repeat: no-repeat;
    background-position-y: top;
    background-position-x: left;
    padding-top: 7%;
}

.feedback-section {
    padding-top: 2%;


}

.news-section {
    padding-bottom: 10%;
}


.bg-battle {
    background-color: #212733;
    padding-top: 5%;
    padding-bottom: 7%
}

.img-container {
    img {
        width: 100%;
    }
}

.my-card-battle {
    background-color: $footer-bg-1;


    .my-card-body {
        background-color: $color-4;
    }
}

.battle-icon {
    padding-top: 15px;

    img {
        padding-left: 15px;
    }

    .versus-icon {
        padding-left: 55px;
        padding-top: 20px;
    }
}

.my-streaming-card {
    background-color: black;
    margin-bottom: 7%;
    position: relative;

    img {
        width: 100%;
        opacity: 0.3;
    }

    .live-icon {
        position: absolute;
        top: 20px;
        right: 20px;

        div {
            margin: 20px;
            padding: 10px;
            background-color: $color-5;

            img {
                display: inline;
                width: 20px;

            }
        }
    }

    .live-play {
        position: absolute;
        top: 350px;
        left: 350px;
    }

    .live-counter {
        position: absolute;
        top: 680px;
        left: 40px;
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