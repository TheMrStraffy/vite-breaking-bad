<script>
import HeaderAppVue from './components/HeaderApp.vue'
import MainAppVue from './components/MainApp.vue'

export default {
  name: "App",
  components: {HeaderAppVue, MainAppVue}
}
</script>

<template>
  <HeaderAppVue/>
  <div class="container">
  <MainAppVue/>

  </div>
</template>


<style lang="scss">
@use './styles/general.scss' as *;




</style>