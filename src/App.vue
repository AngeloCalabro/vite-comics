<template>
  <HeaderComponent/>
  <MainComponent/> 
  <FooterComponent/>
</template>
 
<script>
    import HeaderComponent from './components/HeaderComponent.vue';
    import MainComponent from './components/MainComponent.vue';
    import FooterComponent from './components/FooterComponent.vue';
    export default {
        components: {
            HeaderComponent,
            FooterComponent,
            MainComponent
        }
    }
</script>
 
<style lang="scss" scoped>

</style>