<script>
  import navbar from './components/navbar.vue';
  import AppContent from './components/AppContent.vue';
  import AppFooter from './components/AppFooter.vue';
  

  export default{
    components:{
      navbar,
      AppContent,
      AppFooter,
    }
  }
</script>

<template>

  <navbar></navbar>
  <AppContent></AppContent>
  <AppFooter></AppFooter>

</template>

<style lang="scss">

  @use './styles/general' as *;

</style>
