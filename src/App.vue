<script>
import axios from "axios";
import HeaderAppVue from './components/HeaderApp.vue'
import MainAppVue from './components/MainApp.vue'
import {store} from './data/store'

export default {
  name: "App",
  components: {HeaderAppVue, MainAppVue},
  data(){
    return{
      store
    }
  },
  methods:{
    getCharacters(){
      store.isLoaded = false;
      axios.get(store.apiUrl, {
        params: {
          category: store.categoryToSearch
        }
      })
      .then(result => {
        store.charactersArray = result.data;
        store.isLoaded=true;
      })
      .catch( error => {
        console.log(error);
      })
    }
  },
  mounted(){
    this.getCharacters();
  },
  created(){

  }
}
</script>

<template>
  <HeaderAppVue/>

  <div class="container">
  
  <MainAppVue @searchCategory="getCharacters()"  />

  </div>
</template>


<style lang="scss">
@use './styles/general.scss' as *;




</style>