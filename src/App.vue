<template>
  <div id="app">
    <div id="nav">
      <Index></Index>
      <Home></Home>
      <Bottom></Bottom>
    </div>
    <router-view/>
  </div>
</template>

<script>
  import Index from './components/index'
  import Home from './components/home'
  import Bottom from './components/bottom'
  export default {
    name:'app',
    components:{
      Index,
      Home,
      Bottom
    }
  }
</script>

<style>
  body{
    padding: 0;
    margin: 0;
    position: absolute;
  }

</style>
