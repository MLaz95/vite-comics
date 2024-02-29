<script>
  import navbar from './components/navbar.vue';
  import AppContent from './components/AppContent.vue';

  export default{
    components:{
      navbar,
      AppContent,
    }
  }
</script>

<template>

  <navbar></navbar>
  <AppContent></AppContent>

</template>

<style lang="scss">

  @use './styles/general' as *;

</style>
