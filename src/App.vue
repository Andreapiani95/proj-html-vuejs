<script >
import PageHeader from './components/PageHeader.vue';
import PageMain from './components/PageMain.vue';
import PageFooter from './components/PageFooter.vue';

export default {
  data() {
    return {

    }
  },
  components: {
    PageHeader,
    PageMain,
    PageFooter,
  },
  methods: {

  },
};

</script>

<template>
  <PageHeader />

  <PageMain />

  <PageFooter />
</template>

<style lang="scss">
@use "./scss/style.scss"
</style>
