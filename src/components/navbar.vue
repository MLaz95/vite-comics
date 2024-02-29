<script>
    export default {
        name: 'navbar',

        data(){
            return{
                // array with all the navbar links
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
                ],

                // keeps track of the active navbar link
                activeIndex: 1,
            }
        },

        methods: {

            // updates the active link on click
            showActive(index){
                this.activeIndex = index
            }
        }
    }

</script>

<template>
    <nav>
        <div class="container">
            <!-- logo -->
            <div class="logo-wrapper">
                <img src="/img/dc-logo.png" alt="">
            </div>
            <div>
                <ul>
                    <!-- creates a link for each element in the array -->
                    <li
                        v-for="(link, index) in links"
                        :class="[index == activeIndex ? 'active' : '']"
                        @click="showActive(index)"
                        >{{link.toUpperCase()}}
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<style lang="scss">
    @use '../styles/palette.scss' as *;

    nav{
        // padding: 20px 0;
        background-color: white;

        .container{
            display: flex;
            justify-content: space-between;
            align-items: center;

            ul{
                list-style: none;
                display: flex;

                li{
                    padding: 50px 0.8rem;
                    font-size: 0.8rem;
                    font-weight: bold;
                    cursor: pointer;
                    position: relative;

                    // creates the blue underline underneath each link
                    &.active::after{
                        content: '';
                        width: 70%;
                        height: 5px;
                        background-color: $primary-color;
                        position: absolute;
                        bottom: 0;
                        left: 50%;
                        transform: translateX(-50%);
                    }

                    &:hover, &.active{
                        color: $primary-color;
                    }
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
