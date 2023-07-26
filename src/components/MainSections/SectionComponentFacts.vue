<script>
export default {
    name: 'SectionComponentFacts',
    data() {
        return {
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
    methods: {

    }
}
</script>

<template>
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
</template>

<style lang="scss" scoped>
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
</style>