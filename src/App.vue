<template>
  <div id="app">
    <div id="nav">
<!--      <div class="bg">-->
<!--        <img src="./assets/bimg2.jpg" alt="" style="width: 100%;height: 100%">-->
<!--      </div>-->
      <Index class="top"></Index>
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
    margin: 0;
    padding: 0
  }
  body{
      margin-left: 0px;
      margin-top: 0px;
      margin-right: 0px;
      margin-bottom: 0px;
      background-image: url("./assets/bimg2.jpg");
      background-size: cover;
      background-attachment:fixed;
      background-position: 0 123px;
  }
    .top{
        position: fixed;
        left: 0;
        top: 0;
    }
</style>
