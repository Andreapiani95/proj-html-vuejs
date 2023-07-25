<script>
export default {
    name: 'PageFooter',
    data() {
        return {

        }
    },
    components: {

    },
    methods: {

    }
}
</script>

<template>
    <section class="my-footer-bg-top">
        <div class="container-xl position-relative">
            <div class="card my-footer-card mx-auto">
                <div class="card-body row">
                    <div class="col-7 text-white">
                        <h2>Subscribe Newsletter</h2>
                        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Odit doloribus magni quia dolorum.</p>
                    </div>
                    <div class="col-5">
                        <div class="input-group py-5">
                            <input type="text" class="form-control" placeholder="Username" aria-label="Enter your email"
                                aria-describedby="basic-addon1">
                            <span class="input-group-text" id="basic-addon1"><img src="" alt=""></span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section class="my-footer-bg-bottom">
        <p class="text-center text-white py-4 my-0">
            Copyright &#169; 2022 <span class="my-green-text">FUTIO</span>. ALL rights reserved.
        </p>
    </section>
</template>

<style lang="scss" scoped>
@use "../scss/variables.scss" as *;

.my-footer-bg-top {
    background-color: $footer-bg-1;
}

.my-footer-bg-bottom {
    background-color: $footer-bg-2;
}

.my-footer-card {
    width: 80%;
    border: 1px black;

    div {
        background-color: $color-4;
    }

}

.my-green-text {
    color: $color-2;
}
</style>