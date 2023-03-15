<script>
import Home from './page/Home.vue';

export default{
    name:"App",
    components:{
        Home,
    }
}
</script>


<template>
  <div id="app">
    <Home/>
  </div>
</template>


<style >
  body{
    display: flex;
    flex-direction: row;
    justify-content: start;
  }
</style>
