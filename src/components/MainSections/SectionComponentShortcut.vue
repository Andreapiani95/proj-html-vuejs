<script>
import ButtonComponent from '../ButtonComponent.vue';
export default {
    name: 'SectionComponentShortcut',
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
</template>

<style lang="scss" scoped>
.main-section-1 {
    padding-top: 7%;
    padding-bottom: 7%;
}

.main-section-1-title {
    font-size: 3rem;
    overflow: hidden;
}

.img-container {
    img {
        width: 100%;
    }
}
</style>
