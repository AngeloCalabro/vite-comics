<template>
    <section>
        <div class="container">
            <div class="button">
                <span>Sign-up Now!</span>
            </div>
            <ul>
            <span>follow us</span>
                <li v-for="(link, index) in socials" :key="index">
                    <a :href="link.url">
                    <img :src="getImagePath(`../assets/img/${link.image}`)" :alt="link.text">
                    </a>
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
    export default {
        name: "SocialFooter",
        data(){
            return{
                socials: [
                    {
                        image: 'footer-facebook.png',
                        text: 'facebook',
                        url: '#',
                        status: false
                    },
                    {
                        image: 'footer-twitter.png',
                        text: 'twitter',
                        url: '#',
                        status: true
                    },
                    {
                        image: 'footer-youtube.png',
                        text: 'youtube',
                        url: '#',
                        status: false
                    },
                    {
                        image: 'footer-pinterest.png',
                        text: 'pinterest',
                        url: '#',
                        status: false
                    },
                    {
                        image: 'footer-periscope.png',
                        text: 'periscope',
                        url: '#',
                        status: false
                    }
                ]
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
        background-color: $darkgrey;
        div.container{
            @include center(between);
            div.button{
            color: $white;
            text-transform: uppercase;
            border: 3px solid $blue;
        }
        ul{
            list-style: none;
                @include dflex;
            span{
                color: $blue;
                font-weight: 600;
                text-transform: uppercase;
            }
            li a{
                display: inline-block;
                text-decoration: none;
                font-weight: 400;
                text-transform: uppercase;
                color: $white;
                margin: 1rem;

                @include dflex;
                }
            li img{
                
                &:hover{
                    scale: 0.9;
                }
            }   
        }
        }
        
}
</style>