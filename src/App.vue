<script >
  import AppHeader from './components/Appheader.vue';
  import AppMain from './components/AppMain.vue';
  import AppFooter from './components/AppFooter.vue';
  export default{
    components:{
      AppHeader,
      AppMain,
      AppFooter
    }
  }
</script>

<template>
  <header> 
    <!-- header  -->
    <AppHeader/>
  </header>
  <main>
    <AppMain/>
  </main>
  <footer>
    <AppFooter/>
  </footer>
</template>

<style lang="scss">

</style>
