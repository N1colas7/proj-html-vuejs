<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import FooterApp from './components/FooterApp.vue';


export default{
    components:{
      AppHeader,
      AppContent,
      FooterApp,
    },
    data() {
      return {
        navHead:[
          {
            name:"Home"
          },
          {
            name:"Shop"
          },
          {
            name:"Products"
          },
          {
            name:"Categories"
          },
          {
            name:"News"
          },
          {
            name:"Elements"
          },
        ],
      }
    },

}
</script>

<template lang="">
  <div>
    <AppHeader :navHead=navHead />
    <AppContent />
    <FooterApp />
   </div> 
</template>

<style lang="scss">
  @use './styles/generals.scss' as *

</style>
