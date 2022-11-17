<script>
import SectionAppVue from './SectionApp.vue'

export default {
  name: "MainApp",
  components: {SectionAppVue},
  data(){
    return{

    }
  }
}
</script>

<template>
  <main>
    <div class="selection">

    <select class="form-select" aria-label="Default select example">
    <option selected>Select Category</option>
    <option value="1">All Characters</option>
    <option value="2">Breaking Bad</option>
    <option value="3">Better Call Saul</option>
    </select>
    </div>
    <div class="mc-container">

    <SectionAppVue/>
    </div>
    
  </main>
</template>


<style lang="scss" scoped>
.selection{
  width: 160px;
  height: 40px;
}
.mc-container{
  background-color:white;
}
</style>