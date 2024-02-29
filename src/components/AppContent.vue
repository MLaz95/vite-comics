<script>
    export default {
        name: 'AppContent',

    }

</script>

<template>
    <main>
        <div class="container">
            CONTENT GOES HERE
        </div>
    </main>
</template>

<style lang="scss">
    @use '../styles/palette.scss' as *;


    main{
        padding: 3rem;
        text-align: center;
        color: white;
        background-color: $tertiary-color;
    }

</style>