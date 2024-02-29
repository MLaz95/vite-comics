<script>
    export default {
        name: 'AppLinks',

        data(){
            return{
                links: [
                    {
                        text: 'digital comics',
                        img: '/public/img/buy-comics-digital-comics.png',
                    },{
                        text: 'dc merchandise',
                        img: '/public/img/buy-comics-merchandise.png',
                    },{
                        text: 'subscription',
                        img: '/public/img/buy-comics-subscriptions.png',
                    },{
                        text: 'comic shop locator',
                        img: '/public/img/buy-comics-shop-locator.png',
                    },{
                        text: 'dc power visa',
                        img: '/public/img/buy-dc-power-visa.svg',
                    },
                ]
            }
        }

    }

</script>

<template>
    <div id="AppLinks">
        <div class="container">
            <ul>
                <li v-for="link in links">
                    <div class="link-img-wrapper">
                        <img :src="link.img" alt="">
                    </div>
                    {{ link.text.toUpperCase() }}
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss">
    #AppLinks{
        padding: 3rem 0;

        color: white;
        background-color: #0282F9;

        ul{
            list-style: none;

            display: flex;
            justify-content: space-around;
            gap: 2rem;
            
            li{
                display: flex;
                align-items: center;
                gap: 0.5rem;

                .link-img-wrapper{
                    height: 55px;
                    width: 55px;

                    img{
                        height: 100%;
                        
                        &[src="/public/img/buy-dc-power-visa.svg"]{
                            width: 100%;
                        }
                    }
                }
            }
                
        }
    }
    

</style>