<script>

    export default{
        name: 'ProductItem',

        props: {
            productImage: String,
            productTitle: String,
        }
    }

</script>

<template>

    <div class="card">
        <img :src="productImage" alt="">
        <h5>{{ productTitle.toUpperCase() }}</h5>
    </div>

</template>

<style lang="scss">
    .card{
        width: calc(100% / 6);
        padding: 14px;

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
    }

</style>