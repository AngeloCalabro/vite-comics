<template>
  <HeaderComponent/>
  <main>
    <div>&lt; Content goes here &lt;</div>
  </main>
  <FooterComponent/>
 </template>
 
 <script>
 import HeaderComponent from './components/HeaderComponent.vue';
 import FooterComponent from './components/FooterComponent.vue';
  export default {
    components: {
      HeaderComponent,
      FooterComponent,
    }
    
  }
 </script>
 
 <style lang="scss" scoped>
@use './assets/styles/partials/variables' as *;
@use './assets/styles/partials/mixins' as *;

 main{
  color: $black;
 }

 </style>