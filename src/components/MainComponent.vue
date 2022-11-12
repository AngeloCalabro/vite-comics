<template>
    <main>
        <section class="jumbo">
        </section>
        <section>
            <div class="cards container">
                <h2>Current series</h2>
                <div class="row g-0">
                    <itemsComponent v-for="(item, index) in heroDc" :key="index" :obj="item"/>
                </div>
                <h3 class="button">Load Mode</h3>
            </div>
        </section>
    </main>
</template>

<script>
import  {hero} from '../data/dc-comics';
import itemsComponent from './itemsComponent.vue'
    export default {
        components:{
            itemsComponent
        },
        name: 'MainComponent',
        data(){
            return{
                heroDc : hero
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

main{
    padding-top: 118px;
    background-color: $black;
    
        section.jumbo{
            min-height: 300px;
            background-image: url('../assets/img/jumbotron.jpg');
            background-position: top;
            background-size: cover;
        }
        .cards {
            text-align: center;
            position: relative;
            h2{
                color: $white;
                background-color: $blue;
                display: inline-block;
                padding: 0.5rem;
                position: absolute;
                top: -30px;
                left: 0px;
            }
            .row {
                margin: 3rem auto;
            }
            h3.button{
                color: $white;
                background-color: $blue;
                display: inline-block;
                cursor: pointer
            }
        }
    }

</style>