<script>
import axios from "axios";
import {store} from '../data/store'
export default {
  name:"CardApp",
  
  data(){
    return{
      store
    }
  },
  methods:{
    getCharacters(){
      axios.get(store.apiUrl)
      .then(result => {
        store.charactersArray = result.data;
        console.log(store.charactersArray);
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
  <div 
  v-for="character in store.charactersArray" :key="character.id"
  class="col">

  <div class="mc-card">
    <div class="img-card">
      <img :src="character.img" :alt="character.name">
    </div>
    <h4>{{character.name}}</h4>
    <p>{{character.category}}</p>
    <p>{{character.status}}</p>
  </div>
  </div>
</template>


<style lang="scss" scoped>
@use '../styles/partials/vars' as *;
.mc-card{
  width: 230px;
  height: 400px;
  margin-bottom: 20px;
  padding-top: 20px;
  background-color: $brPrimaryColor;
  text-align: center;
  .img-card{
    width: 100%;
    text-align: center;
    img{
      
      width: 180px;
      
    }
  }
}
h4{
  color:white;
}
p{
  color: #7d7967;
}

</style>