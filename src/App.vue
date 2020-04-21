<template>
  <div id="app">
    <div id="nav">
      <Index></Index>
<!--      <Home></Home>-->
      <Home2></Home2>
      <Bottom></Bottom>
    </div>
    <router-view/>
  </div>
</template>

<script>
  import Index from './components/index'
  import Home from './components/home'
  import Bottom from './components/bottom'
  import Home2 from './components/home2'
  export default {
    name:'app',
    components:{
      Index,
      Home,
      Bottom,
      Home2
    }
  }
</script>

<style>

  html,body{
    width:100%;
    margin: 0;
    background: yellow;
    box-sizing: border-box;
    /*padding-bottom: 20px;*/
  }
</style>
