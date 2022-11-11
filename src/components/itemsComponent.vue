<template>
    <div class="col-lg-2 col-md-4 col-sm-6">
        <div class=" card">
            <img class="img-card" :src="obj.thumb" :alt="obj.titolo">
        </div>
        <h6>{{obj.series}}</h6>
    </div>
</template>

<script>

    export default {
        name: 'itemsComponent',

        props: [
            'obj'
        ]
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;


h6{
    color: $white;
}
</style>