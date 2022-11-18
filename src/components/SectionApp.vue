<script>
import {store} from '../data/store'
import CardAppVue from './CardApp.vue'
export default {
  name: "SectionApp",
  components: {CardAppVue},
  data(){
    return{
      store
    }
  },
  computed:{
    totalFound(){
      return store.charactersArray.length;
    }
  }
  
}
</script>

<template>

<section class="container p-5">

  <div class="foundBar">
    <h4>Found {{totalFound}} characters</h4>
  </div>
  <div class="row">

  <CardAppVue :characters="store.charactersArray" />
  </div>

</section>
</template>


<style lang="scss" scoped>


</style>