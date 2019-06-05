<template>
  <div id="app">
    <Home></Home>
    <About></About>
    <div class="a">
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
import Home from './views/Home'
import About from './views/About'

export default {
  name:'app',
  components:{Home,About},
  data() {
    return {
      msg:"ss"
    }
  },
}
</script>

<style>
*{
  padding:0;
  margin:0;
}
.a{
  position: absolute;
  top:60px;
  left:200px;
  bottom:0;
  right:0;
}
</style>
