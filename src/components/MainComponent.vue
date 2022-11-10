<template>
    <main>
        <div>--&gt; Content goes here &lt;--</div>
    </main>
</template>

<script>
    export default {
        name: 'MainComponent',
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

main{
    min-height: 300px;
    padding-top: 130px;
    background-color: $black;
    color: $white;
    div{
        text-align: center;
        text-transform: uppercase;
    }
    }

</style>