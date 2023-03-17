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
    font-family: 'Roboto', sans-serif;
    font-family: 'Roboto';
    font-style: normal;
    font-weight: 400;
}
  body{
    display: flex;
    flex-direction: row;
    justify-content: start;
  }
</style>
