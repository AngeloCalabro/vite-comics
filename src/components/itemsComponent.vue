<template>
    <div class="cols col-lg-2 col-md-3 col-sm-4">
        <div class="card">
            <img class="img-card img-fluid" :src="obj.thumb" :alt="obj.titolo">
        </div>
        <div class="text-img">{{obj.series}}</div>
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
div.cols{
    text-align: center;
    div.card{
        width: 150px;
        height: 150px;
        margin: 1rem;
        img.img-card{
            overflow: hidden;
            object-fit: cover;
            object-position: top;
            border-radius: 5px;
        }
    }
    div.text-img{
        color: $white;
        margin-top: 1rem;
        text-align: start;
        text-transform: uppercase;
        font-size: $fs-s;
        margin: 1rem;
    }
}
</style>