<template>
    <header>
        <div class="container">
            <a href="">
                <img src="../assets/img/dc-logo.png" alt="logo">
            </a>
            <ul>
                <li v-for="(link, index) in linksNavBar" :key="index" :class="{'active' : link.status}">
                    <a :href="link.url" >{{link.text}}</a>
                </li>
            </ul>
        </div>
    </header>
</template>

<script>
import  {links} from '../data/dc-comics';
    export default {
        name: 'HeaderComponent',
        data(){
            return{
                linksNavBar : links,
                // links: [
                //     {
                //         text: 'characters',
                //         url: '#',
                //         status: false
                //     },
                //     {
                //         text: 'comics',
                //         url: '#',
                //         status: true
                //     },
                //     {
                //         text: 'movies',
                //         url: '#',
                //         status: false
                //     },
                //     {
                //         text: 'tv',
                //         url: '#',
                //         status: false
                //     },
                //     {
                //         text: 'games',
                //         url: '#',
                //         status: false
                //     },
                //     {
                //         text: 'collectibles',
                //         url: '#',
                //         status: false
                //     },
                //     {
                //         text: 'videos',
                //         url: '#',
                //         status: false
                //     },
                //     {
                //         text: 'fans',
                //         url: '#',
                //         status: false
                //     },
                //     {
                //         text: 'news',
                //         url: '#',
                //         status: false
                //     },
                //     {
                //         text: 'shop',
                //         url: '#',
                //         status: false
                //     },
                // ]
            }
        }
    }
</script>

<style lang="scss">
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

    header{
        width: 100%;
        height: 118px;
        background-color: $white;
        text-align: center;
        position: fixed;
        z-index: 1000;
        div{
            height: 100%;
            @include center(between);
            a{
                display: inline-block;
            }
            ul{
                list-style: none;
                margin: 2.5rem 1rem 4rem;
                @include dflex;
                li a{
                    display: inline-block;
                    padding: 1rem;
                    text-decoration: none;
                    font-weight: 600;
                    text-transform: uppercase;
                    color: $black;
                    transition: color 0.3s;
                    font-size: $fs-s;

                    &.active,
                    &:hover {
                        color: $blue;
                        border-bottom: 3px solid $blue;
                    }
                }
            }
        }
    }

</style>