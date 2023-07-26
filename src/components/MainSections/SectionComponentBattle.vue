<script>
import ButtonComponent from '../ButtonComponent.vue';
export default {
    name: 'SectionComponentbattle',
    data() {
        return {
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
        }

    },
    components: {
        ButtonComponent
    },
    methods: {

    }
}
</script>

<template>
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
</template>

<style lang="scss" scoped>
@use "../src/scss/variables.scss" as *;

.battle-section-title {
    font-size: 3.5rem;
}

.bg-battle {
    background-color: #212733;
    padding-top: 5%;
    padding-bottom: 7%
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
</style>