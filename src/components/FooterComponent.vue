<template>
    <footer>
        <BannerFooter/>
        <CenterFooter/>
        <SocialFooter/>    
    </footer>
</template>

<script>
import BannerFooter from './BannerFooter.vue';
import CenterFooter from './CenterFooter.vue';
import SocialFooter from './SocialFooter.vue';
    export default {
    name: "FooterComponent",
    components: { BannerFooter, CenterFooter, SocialFooter }
}
    
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;
footer{
    position: fixed;
    bottom: 0;
    right: 0;
    left: 0;
}

</style>