<script>
export default {
  name: "HeaderApp",
  data(){
    return{

    }
  }
}
</script>

<template>
  <header class="d-flex align-items-center">
    <div class="logo">
      <img src="/BBlogo.png" alt="breaking bad logo">
    </div>
    <h1>Breaking Bad Api</h1>
  </header>
</template>


<style lang="scss" scoped>
header{
  margin-bottom: 20px;
}
.logo{
  width: 50px;
  height: 50px;
  img{
    height: 100%;
  }
}
h1{
  color: white;
}
</style>