<script>
    import AppLinks from './AppLinks.vue';


    export default{
        name: 'AppFooter',
        components: {
            AppLinks,
        },
        
        data(){
            return{
                lists: [
                    {
                        name: 'dc comics',
                        links:['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
                    },{
                        name: 'shop',
                        links:['Shop DC', 'Shop DC Collectibles']
                    },{
                        name: 'dc',
                        links:['Terms of Use', 'Privacy Policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshop', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us']
                    },{
                        name: 'sites',
                        links:['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
                    },
                ],

                socials: [
                    {
                        name: 'facebook',
                        icon: '/img/footer-facebook.png'
                    },{
                        name: 'twitter',
                        icon: '/img/footer-twitter.png'
                    },{
                        name: 'youtube',
                        icon: '/img/footer-youtube.png'
                    },{
                        name: 'pinterest',
                        icon: '/img/footer-pinterest.png'
                    },{
                        name: 'periscope',
                        icon: '/img/footer-periscope.png'
                    },
                ]
            }
        }
    }

    
    
</script>

<template>
    <AppLinks></AppLinks>

    <footer>
        <div class="ft-top">
            <div class="container">
                
                <ul class="list-container">
                    <!-- creates a list item for each element in lists -->
                    <li v-for="list in lists">
                        <h2 class="list-head">{{list.name.toUpperCase()}}</h2>
                        <ul>
                            <!-- inside each list it creates a nested list taking items from the links array -->
                            <li v-for="link in list.links" class="list-item">
                                <a href="#!">{{ link }}</a>
                            </li>
                        </ul>
                    </li>
                </ul>

                <img src="../../public/img/dc-logo-bg.png" alt="" class="bg-logo">
            </div>
        </div>

        <!-- link socials -->
        <div class="ft-bottom">
            <div class="container">
                <button>sign-up now!</button>
                <div class="ft-socials">
                    <h3>follow us</h3>
                    <ul>
                        <li v-for="social in socials">
                            <img :src="social.icon" alt="">
                        </li>
                    </ul>
                </div>
            </div>

        </div>
    </footer>
</template>

<style lang="scss">
    @use '../styles/palette.scss' as *;

    footer{
        color: white;
        background-color: $secondary-color;

        ul{
            list-style: none;
            padding: 0;
        }

        .ft-top{
            padding: 55px 0 65px;
            background-image: url(/img/footer-bg.jpg);
            background-size: cover;
            overflow: hidden;

            .list-container{
                display: flex;
                flex-direction: column;
                flex-wrap: wrap;
                align-content: start;
                column-gap: 3rem;

                max-height: 370px;
            }

            .list-head{
                font-size: 1em;
                padding: 0.5em 0;
            }

            .list-item{
                font-size: 0.8rem;
                color: gray;

                a{
                    color: gray;
                    text-decoration: none;
                    &:hover{
                        text-decoration: underline;
                    }
                }
            }

            .container{
                position: relative;
            }

            .bg-logo{
                position: absolute;
                right: 0;
                top: -50%;
            }
        }

        .ft-bottom{
            background-color: $secondary-color;
            padding: 2rem;

            .container{
                display: flex;
                justify-content: space-between;

                button{
                    background: transparent;
                    border: 2px solid $primary-color;
                    text-transform: uppercase;
                    
                    color: white;
                    font-weight: bold;
                    font-size: 1rem;
                    padding: 1rem;

                    cursor: pointer;
                    transition: background-color 0.3s;

                    &:hover{
                        background-color: $primary-color;
                    }
                }

                .ft-socials{
                    display: flex;
                    align-items: center;
                    gap: 1rem;

                    h3{
                        text-transform: uppercase;
                        color: $primary-color;
                    }

                    ul{
                        display: flex;
                        align-items: center;
                        gap: 1rem;

                        li{
                            widows: 35px;
                            height: 35px;

                            cursor: pointer;

                            img{
                                width: 100%;
                            }
                        }
                    }
                }
            }
        }
    }
    

</style>