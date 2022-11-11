<template>
    <main>
        <section class="jumbo">
        </section>
        <section>
            <div class="cards container">
                <h1>Current series</h1>
                <div class="row">
                    <itemsComponent v-for="(item, index) in heroDc" :key="index" :obj="item"/>
                </div>
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
            h1{
                color: $white;
            }
            .row {
                @include dflex;
                .col {
                    flex-basis: calc(100% / 6);
                    // padding: 2rem;
                    }
            }
        }
    }

</style>