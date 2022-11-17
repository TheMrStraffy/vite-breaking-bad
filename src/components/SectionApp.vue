<script>
import CardAppVue from './CardApp.vue'
export default {
  name: "SectionApp",
  components: {CardAppVue},
  data(){
    return{
    }
  }
}
</script>

<template>

<section class="container p-5">

  <div class="foundBar">
    <h4>Found 62 characters</h4>
  </div>
  <div class="row">

  <CardAppVue/>
  </div>

</section>
</template>


<style lang="scss" scoped>


</style>