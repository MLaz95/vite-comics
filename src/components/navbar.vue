<script>
    export default {
        name: 'navbar',

        data(){
            return{
                links: [
                    'characters',
                    'comics',
                    'movies',
                    'tv',
                    'games',
                    'collectibles',
                    'videos',
                    'fans',
                    'news',
                    'shop',
                ]
            }
        }
    }

</script>

<template>
    <nav>
        <div class="container">
            <div class="logo-wrapper">
                <img src="../../public/img/dc-logo.png" alt="">
            </div>
            <div>
                <ul>
                    <li v-for="link in links">{{link.toUpperCase()}}</li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<style lang="scss">

    nav{
        padding: 20px 0;
        background-color: white;

        .container{
            display: flex;
            justify-content: space-between;
            align-items: center;

            ul{
                list-style: none;
                display: flex;

                li{
                    padding: 0 0.8rem;
                }
            }
        }
    }

    .logo-wrapper{
        max-width: 80px;
        max-height: 80px;

        img{
            width: 100%;
        }
    }

</style>
