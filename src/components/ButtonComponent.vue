<script>
export default {
    name: 'ButtonComponent',
    data() {
        return {

        }
    },
    props: {
        buttonText: String,
    },
    methods: {

    }
}
</script>

<template>
    <button class="btn text-black my-button fw-bold">
        {{ buttonText }}
        <span v-show="buttonText !== 'LIVE STREAMING'">
            <img src="img/svg/e-double-right-arrow.svg" alt="">
        </span>
    </button>
</template>

<style lang="scss" scoped>
@use "../scss/variables.scss" as *;

.my-button {
    border-radius: 15% / 50%;
    padding: 10px;
    background-color: $color-1;
    border: 3px solid black;
    outline: 1px solid $color-1;

    span {
        img {
            filter: invert(1);
        }
    }
}

.my-button:hover {
    background-color: $color-2;
    outline-color: $color-2;
}
</style>