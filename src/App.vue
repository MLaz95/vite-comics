<script>
  import navbar from './components/navbar.vue';
  import AppContent from './components/AppContent.vue';
  import AppLinks from './components/AppLinks.vue';
  

  export default{
    components:{
      navbar,
      AppContent,
      AppLinks,
    }
  }
</script>

<template>

  <navbar></navbar>
  <AppContent></AppContent>
  <AppLinks></AppLinks>


</template>

<style lang="scss">

  @use './styles/general' as *;

</style>
