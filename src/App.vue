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
    <!-- header -->
    <AppHeader/>
  </header>
  <main>
    <!-- main -->
    <AppMain/>
  </main>
  <footer>
    <!-- footer -->
    <AppFooter/>
  </footer>
</template>

<style lang="scss">
header{
  background-color: #1c1c1c;

}
  
</style>
