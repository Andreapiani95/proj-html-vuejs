<script>
import ButtonComponent from './ButtonComponent.vue';
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
        }
    },
    components: {
        ButtonComponent,

    },
    methods: {

    }
}
</script>

<template>
    <main class="my-0">
        <section class="bg-black">
            <div class="container-xl">
                <div class="row">
                    <div class="col-6">
                        <div class="img-container">
                            <img src="img/features-illus.png" alt="">
                        </div>
                    </div>
                    <div class="col-6 text-white">
                        <h4 class="my-green-text">The Ultimate Competitive Gaming Platform</h4>
                        <h2>Make Your Own Mark On The Battle Field</h2>
                        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Consectetur, exercitationem perferendis
                            nihil quibusdam optio vitae voluptatibus debitis ipsam, enim rerum facere nam reiciendis dolore
                            aliquam ex in laboriosam quasi repellat!
                        </p>
                        <div>
                            <div v-for="(element, index) in  shortcutSection " class="row">
                                <div class="col-3">
                                    <img :src="element.path" alt="  ">
                                </div>
                                <div class="col-9">
                                    <h4>{{ element.title }}</h4>
                                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque cum pariatur
                                        aspernatur commodi quia? Doloremque?</p>
                                </div>
                            </div>
                        </div>
                        <ButtonComponent />
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-battle">
            <div class="container-xl">
                <div class="row justify-content-center text-center">
                    <div class="col-5">
                        <h4 class="my-green-text">Trending Battle</h4>
                        <h2 class="text-white">
                            Keep Eyes & Manage Upcoming Battle
                        </h2>
                        <p class="text-light">
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor sit
                            ullam
                            placeat reiciendis
                            ducimus optio vel at corporis, omnis magni.
                        </p>
                    </div>
                </div>
                <div class="row">
                    <div v-for="(element, index) in battleSection" class="col-6">
                        <div class="card my-card-battle">
                            <div class="row justify-content-around">
                                <div class="col-4">
                                    <img :src="element.team1" alt="">
                                </div>
                                <div class="col-4">
                                    <img src="img/versus-icon.png" alt="">
                                </div>
                                <div class="col-4">
                                    <img :src="element.team2" alt="">
                                </div>
                            </div>
                            <div class="card-body text-center my-card-body">
                                <p class="card-text">
                                <h3 class="text-white">{{ element.title }}</h3>
                                <p class="my-green-text">December 25, 2022 4:00 PM</p>
                                </p>
                            </div>
                            <div class="card-body row justify-content-center text-white">
                                <div class="col-5">
                                    <span>
                                        <img src="img/icon/youtube-icon.png" alt="">
                                    </span>
                                    <span>
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
                <div class="text-center">
                    <ButtonComponent />
                </div>

            </div>
        </section>

        <section class="bg-black">
            <div class="container-xl">
                <h2 class="text-center text-white">Futio Quick Facts</h2>
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
    </main>
</template>

<style lang="scss" scoped>
@use "../scss/variables.scss" as *;

.bg-battle {
    background-color: #212733;
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
</style>