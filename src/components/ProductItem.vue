<script>

    export default{
        name: 'ProductItem',

        props: {
            productImage: String,
            productTitle: String,
            productPrice: String,
        }
    }

</script>

<template>

    <div class="card">
        <img :src="productImage" alt="">
        <h5>{{ productTitle.toUpperCase() }}</h5>
        <div class="card-overlay">
            <div class="price">{{ productPrice }}</div>
            <button>Add to Cart</button>
        </div>
    </div>

</template>

<style lang="scss">
    .card{
        width: calc(100% / 6);
        padding: 14px;
        position: relative;

        img{
            width: 100%;
            aspect-ratio: 1 / 1;
            object-fit: cover;
            object-position: top;
        }

        h5{
            font-weight: normal;
            padding: 0.5em 0;
        }

        &:hover .card-overlay{
                opacity: 1;
                pointer-events: all;
            }

        .card-overlay{
            width: 100%;
            height: 100%;

            position: absolute;
            top: 0;
            left: 0;

            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;

            background-color: rgba($color: #000000, $alpha: 0.5);

            opacity: 0;
            pointer-events: none;
            transition: opacity 0.3s;

            .price{
                font-size: 1.5rem;
            }

            button{
                width: 80%;
                margin: 1rem;
                padding: 1rem;

                background-color: transparent;
                text-wrap: nowrap;
                border: 1px solid white;
                
                transition: background-color 0.3s;

                &:hover{
                    background-color: #0282F9;
                }
            }
        }
    }

</style>