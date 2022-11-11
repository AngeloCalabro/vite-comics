<template>
    <section>
        <div class="container">
            <div class="cols">
                <div class="row">
                    <div class="col-4">
                        <ul>
                            <h5>DC Comics</h5>
                            <li v-for="(link, index) in links" :key="index">
                            <a :href="link.url" :class="{'active' : link.status}">{{link.text}}</a>
                            </li>
                        </ul>
                        <ul>
                            <h5>Shop</h5>
                            <li v-for="(link, index) in shop" :key="index">
                            <a :href="link.url" :class="{'active' : link.status}">{{link.text}}</a>
                            </li>
                        </ul>
                    </div>
                    <ul class="col-4">
                        <h5>Shop</h5>
                            <li v-for="(link, index) in linksDc" :key="index">
                            <a :href="link.url" :class="{'active' : link.status}">{{link.text}}</a>
                            </li>
                    </ul>
                    <ul class="col-4">
                        <h5>Sites</h5>
                            <li v-for="(link, index) in sites" :key="index">
                            <a :href="link.url" :class="{'active' : link.status}">{{link.text}}</a>
                            </li>
                    </ul>
                </div>
            </div>
            <div class="cols logo-img">
                <img class="image-dc" src="../assets/img/dc-logo-bg.png" alt="logo">
            </div>
        </div>
        
    </section>
</template>

<script>
    export default {
        name: "CenterFooter",
        data(){
            return{
                links: [
                    {
                        text: 'characters',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'comics',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'movies',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'tv',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'games',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'collectibles',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'videos',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'fans',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'news',
                        url: '#',
                        status: false
                    }
                ],
                shop: [
                    {
                        text: 'Shop DC',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'Shop DC Collectibles',
                        url: '#',
                        status: false
                    },
                ],
                linksDc: [
                    {
                        text: 'Terms Of use',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'Privacy policy (New)',
                        url: '#',
                        status: true
                    },
                    {
                        text: 'Ad Choises',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'Advertising',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'Jobs',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'Subscriptions',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'Talent Workshops',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'CPSC Certificates',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'Ratings',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'Shop Help',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'Contact Us',
                        url: '#',
                        status: false
                    }
                ],
                sites: [
                    {
                        text: 'DC',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'MAD Magazine',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'DC Kids',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'DC Universe',
                        url: '#',
                        status: false
                    },
                    {
                        text: 'DC Power Visa',
                        url: '#',
                        status: false
                    }
                ]

            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

    section{
        background-image: url(../assets/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
        div.container{
            @include center();
            div.cols{
                // @include center(vertical);
                ul{
                    list-style: none;
                }
            }
                h5{
                    color: $white;
                    font-weight: 600;
                    text-transform: uppercase;
                    padding-bottom: 1rem;
                }
                li a{
                    display: inline-block;
                    text-decoration: none;
                    text-transform: capitalize;
                    font-size: $fs-s;
                    color: $grey;
                    transition: color 0.3s;

                    &:hover {
                        color: $blue;
                    }
                }
            
            div.logo-img{
                img.image-dc{
                overflow-y: hidden;
                object-position: center;
                }
            }
        }
    }
</style>