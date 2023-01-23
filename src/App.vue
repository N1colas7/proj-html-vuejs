<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import FooterApp from './components/FooterApp.vue';

export default{
    components:{
      AppHeader,
      AppContent,
      FooterApp,
    }
}
</script>

<template lang="">
  <div>
    <AppHeader />
    <AppContent />
    <FooterApp />
   </div> 
</template>

<style lang="scss">
  @use './styles/generals.scss' as *

</style>
