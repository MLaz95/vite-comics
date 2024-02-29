<script>
  import navbar from './components/navbar.vue';
  import AppContent from './components/AppContent.vue';
  import AppLinks from './components/AppLinks.vue';
  import AppFooter from './components/AppFooter.vue';
  

  export default{
    components:{
      navbar,
      AppContent,
      AppLinks,
      AppFooter,
    }
  }
</script>

<template>

  <navbar></navbar>
  <AppContent></AppContent>
  <AppLinks></AppLinks>
  <AppFooter></AppFooter>

</template>

<style lang="scss">

  @use './styles/general' as *;

</style>
