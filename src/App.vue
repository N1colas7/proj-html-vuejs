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
            name:"ciccio"
          },
          {
            name:"ciccio2"
          }
        ]
      }
    },

}
</script>

<template lang="">
  <div>
    <AppHeader v-for="item in navHead" :name="item.name"/>
    <AppContent />
    <FooterApp />
   </div> 
</template>

<style lang="scss">
  @use './styles/generals.scss' as *

</style>
