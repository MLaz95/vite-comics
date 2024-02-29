<script>
    export default{
        name: 'AppFooter',

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
                ]
            }
        }
    }

    
    
</script>

<template>
    <footer>
        <div class="ft-top">
            <div class="container">
                
                <ul class="list-container">
                    <li v-for="list in lists">
                        <h2 class="list-head">{{list.name.toUpperCase()}}</h2>
                        <ul>
                            <li v-for="link in list.links" class="list-item">{{ link }}</li>
                        </ul>
                    </li>
                </ul>

                <img src="../../public/img/dc-logo-bg.png" alt="" class="bg-logo">
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
            background-image: url(../../public/img/footer-bg.jpg);
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

        
    }
    

</style>