<template>
  <el-row type="flex" class="row-bg" justify="center">
    <el-col :span="14">
      <div class="grid-content bg-purple">
        <el-tabs type="border-card" class="el-tabs__item" style="height: 500px;width: 100%;">
          <el-tab-pane class="floor" label="房源推荐" style="">
            <span slot="label"><i class="el-icon-warning"></i> 房源推荐</span>
            <EstateTable></EstateTable>
          </el-tab-pane>
          <el-tab-pane class="el-tabs__header" label="本周高性价比楼盘TOP6"><EstateTable></EstateTable></el-tab-pane>
          <el-tab-pane class="el-tabs__header" label="热销楼盘"><EstateTable></EstateTable></el-tab-pane>
          <el-tab-pane class="el-tabs__header" label="精选楼盘"><EstateTable></EstateTable></el-tab-pane>
        </el-tabs>
      </div>
    </el-col>
    <!--第一层 右侧栏：帮你选房-->
    <el-col :span="4">
      <div class="grid-content-right">
        <el-card class="box-card">
          <div slot="header" class="clearfix">
            <span slot="label" style="float: left;margin-top: -10px;color: red;"><i class="el-icon-date"></i> 帮你选房</span>
          </div>
          <div style="background-color: #f8f7f7;height: 100%" class="form-d">
            <EstateForm></EstateForm>
          </div>
        </el-card>
      </div>
    </el-col>
  </el-row>
</template>

<script>
  import EstateTable from "./EstateTable";
  import EstateForm from "./EstateForm";
    export default {
        name: "Layer_1st",
      components:{
        EstateTable,
        EstateForm
      }
    }
</script>

<style scoped>

  .bg-purple-dark {
    background: #99a9bf;
  }
  .bg-purple {
    background: #f504b5;
  }
  .bg-purple-light {
    background: #025bfa;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
/*  标签页  */


  .row-bg>>>.el-tabs--card>.el-tabs__header {
    border-bottom: 1px solid #f5043c;
    background-color: #9604ff;
  }
  .row-bg>>>.el-tabs--border-card>.el-tabs__header {
    background-color: #F5F7FA;
    border-bottom: 1px solid #f90606;
    margin: 0;
  }
  .el-tabs__item {
    padding: 0 0px;
    height: 40px;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    line-height: 40px;
    display: inline-block;
    list-style: none;
    font-size: 15px;
    font-weight: 500;
    color: #03ff03;
    /*background-color: #f5043c;*/
    position: relative;
  }
  .row-bg>>>.el-tabs--border-card>.el-tabs__content {
    padding: 0px;
  }
  .row-bg[data-v-fa2fa134] {
    padding: 0px 0;
    background-color: #f9fafc;
  }
  .row-bg>>>.el-tabs__item .floor{
    color: #f7f8f9;
    background-color: #f50707;
    border-right-color: #DCDFE6;
    border-left-color: #DCDFE6;
    font-size: large;
  }
  .row-bg>>>.el-tabs--border-card>.el-tabs__header .el-tabs__item.is-active {
    color: #ffffff;
    background-color: #fc0606;
    border-right-color: #DCDFE6;
    border-left-color: #DCDFE6;
  }
  .row-bg>>>.el-tabs__item {
    /*padding: 0 20px;*/
    height: 40px;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    line-height: 40px;
    display: inline-block;
    list-style: none;
    font-size: 14px;
    font-weight: 500;
    color: #303133;
    position: relative;
  }
/*右侧卡片布局样式*/
  .box-card>>> .el-card__header {
    /* padding: 18px 20px; */
    border-bottom: 1px solid #f52807;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    height: 40px;
  }
  .box-card>>> .el-card__body {
     padding: 0px;
  }
  .text {
    font-size: 14px;
  }

  .item {
    margin-bottom: 18px;
  }

  .clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }
  .clearfix:after {
    clear: both
  }

  .box-card {
    width: 100%;
  }
</style>
