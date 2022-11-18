<script>
import {store} from '../data/store'
import LoadingApp from './LoadingApp.vue'
import SectionAppVue from './SectionApp.vue'

export default {
  name: "MainApp",
  components: {SectionAppVue, LoadingApp},
  data(){
    return{
      store
    }
  }
}
</script>

<template>
  <main>
    <div class="selection">

    <select v-model="store.categoryToSearch" class="form-select" @change="$emit('searchCategory')">
    <option value = "" selected>All Characters</option>
    <option value="Breaking Bad">Breaking Bad</option>
    <option value="Better Call Saul">Better Call Saul</option>
    </select>
    </div>
    <div v-if="!store.isLoaded" class="mc-container d-flex justify-content-center align-items-center">
    <LoadingApp />
    </div>
    <div v-else class="mc-container">
    <SectionAppVue  />
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