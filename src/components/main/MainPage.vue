<template>
  <el-container class="main-container">
    <el-header>


      <Header></Header>
    </el-header>
    <el-main>
      <MainBody></MainBody>
    </el-main>
    <el-footer style="height: 80px;"><Footer></Footer></el-footer>
<!--    <el-backtop target=".page-component__scroll .el-scrollbar__wrapr" visibility-height="50"></el-backtop>-->
  </el-container>

</template>

<script>
  import Header from "../common/Header";
  import Footer from "../common/Footer";
  import MainBody from "../main/MainBody";
    export default {
        name: "MainPage",
      components: {Header,MainBody,Footer},
    }
</script>

<style scoped>
  /*.main-container{*/
  /*  width:100%;*/
  /*  height:100vh;*/
  /*  overflow-x:hidden ;*/
  /*}*/

  .el-header {
    background-color: #fa0000;
    color: #333;
    text-align: center;
    line-height: 60px;
  }
  .el-footer{
    background-color: #2b2b2b;
    color: #fcfbfb;
    text-align: center;
    line-height: 60px;
  }


  .el-main {
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
    /*line-height: 160px;*/
    padding: 0px
  }

  body > .el-container {
    margin-bottom: 40px;
  }

  .el-container:nth-child(5) .el-aside,
  .el-container:nth-child(6) .el-aside {
    line-height: 260px;
  }

  .el-container:nth-child(7) .el-aside {
    line-height: 320px;
  }
</style>
