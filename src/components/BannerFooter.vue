<template>
    <section>
        <div class="container">
            <ul>
                <li v-for="(link, index) in linksFooterTop" :key="index">
                    <a :href="link.url">
                    <img :src="getImagePath(`../assets/img/${link.image}`)" :alt="link.text">
                    <span>{{link.text}}</span>
                    </a>
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
import  {linksFooter} from '../data/dc-comics';
    export default {
        name: "BannerFooter",
        data(){
            return{
                linksFooterTop:linksFooter,
                // linksFooter: [
                //     {
                //         image: 'buy-comics-digital-comics.png',
                //         text: 'digital comics',
                //         url: '#',
                //         status: false
                //     },
                //     {
                //         image: 'buy-comics-merchandise.png',
                //         text: 'dc merchandise',
                //         url: '#',
                //         status: true
                //     },
                //     {
                //         image: 'buy-comics-subscriptions.png',
                //         text: 'subscription',
                //         url: '#',
                //         status: false
                //     },
                //     {
                //         image: 'buy-comics-shop-locator.png',
                //         text: 'comic shop location',
                //         url: '#',
                //         status: false
                //     },
                //     {
                //         image: 'buy-dc-power-visa.svg',
                //         text: 'dc power visa',
                //         url: '#',
                //         status: false
                //     }
                // ]
            }
        },
        methods :{
            getImagePath: function(imgPath){
                return new URL (imgPath, import.meta.url).href;
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

section{
    background-color: $blue;
    ul{
            list-style: none;
            @include dflex;

            li a{
                display: inline-block;
                text-decoration: none;
                font-weight: 400;
                text-transform: uppercase;
                color: $white;
                padding: 0.5rem;

                @include dflex;
            }
            li img{
                width: 50px;
                padding-right: 0.5rem;
            }
    }
}

</style>