<script>
import PlayComponent from '../PlayComponent.vue';
export default {
    name: 'SectionComponentStreaming',
    data() {
        return {

        }
    },
    components: {
        PlayComponent,
    },
    methods: {

    }
}
</script>

<template>
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
</template>

<style lang="scss" scoped>
@use "../src/scss/variables.scss" as *;

.streaming-section-title {
    font-size: 3.5rem;
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
</style>