<script>
export default {
    name: 'ButtonComponent',
    data() {
        return {

        }
    },
    methods: {

    }
}
</script>

<template>
    <button class="btn text-black my-button">
        premi
    </button>
</template>

<style lang="scss" scoped>
@use "../scss/variables.scss" as *;

.my-button {
    border-radius: 25% / 50%;
    padding: 10px;
    background-color: $color-1;
    border: 3px solid black;
    outline: 1px solid $color-1;
}
</style>