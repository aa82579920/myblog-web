<template>
  <el-container id="app">
    <el-aside width="240px">
      <LeftNavMenu id="leftNavMenu"></LeftNavMenu>
    </el-aside>
    <Main></Main>
    <el-aside width="240px">
      <RightNavMenu id="rightNavMenu"></RightNavMenu>
    </el-aside>
  </el-container>

</template>

<script>
import LeftNavMenu from "@/components/mainPage/leftNavMenu"
import Main from "@/components/mainPage/main";
import RightNavMenu from "@/components/mainPage/rightNavMenu"
export default {
  name: 'App',
  components: {
    Main,
    LeftNavMenu,
    RightNavMenu
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
#leftNavMenu {
  position:  fixed;
  left: 0px;
  top: 0px;
}
  #rightNavMenu {
    position:  fixed;
    top: 0px;
  }
</style>
