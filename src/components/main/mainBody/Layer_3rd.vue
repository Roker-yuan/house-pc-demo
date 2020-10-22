<template>
  <el-row type="flex" class="row-bg2" justify="center">
    <el-col :span="14">
      <el-row type="flex" class="row-left" justify="center">
        <el-col :span="2" style="background-color: #f5043c;border-top-left-radius: 20px;display:flex">
          <div style="margin:auto">
            <span slot="label" class="card-title" style="font-size: large;color: white;align-content: center">
            <i class="el-icon-warning"></i>洋房·别墅推荐</span>
          </div>
        </el-col>
        <el-col :span="7">
          <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="">
            <el-menu-item index="1">洋房</el-menu-item>
            <el-menu-item index="3">别墅</el-menu-item>
          </el-menu>
        </el-col>
        <el-col :span="1" style="display: flex;font-size: small;background-color: white">
          <div style="width: 100%;text-align: center;display: inline-grid;">
            <el-link style="float: right" :underline="false" href="http://www.baidu.com" >更多>></el-link>
          </div>
        </el-col>
      </el-row>

      <el-row style="margin-left: 0px">
        <!--第三层 左侧栏：楼盘展示-->
        <el-col :span="6" v-for="(o, index) in 8" :key="o" :offset="index % 3 ==0 ? 0 : 0.75" style="margin-top: 20px">
          <el-card :body-style="{ padding: '5px' }">
            <img src="http://www.shoulouxx.com/images/jyzjdy9.jpg" class="image" style="height: 150px;width: 100%">
            <div style="padding: 5px;">
              <span style="float: left;font-size: small;font-weight: bold">龙湖时代上城</span>
              <span style="float: right;font-size: small;color: #475669">建邺区</span>
              <br>
              <hr>
              <div style="font-size: 10px;padding-bottom: 15px">
                <span style="float: left">建面：<span style="color: #f5043c">90+ </span>㎡</span>
                <span style="float: right">均价：<span style="color: #f5043c">26900 </span>元/㎡</span>
              </div>
            </div>
          </el-card>
        </el-col>
      </el-row>


      <!--第二层 左侧底部栏：房源卡片-->
      <div class="row-card">

      </div>
    </el-col>
    <!--***********************************************  第二层：右侧栏    ******************************************************-->
    <!--第一层 右侧栏：帮你选房-->
    <el-col :span="4">
      <div class="third-content-right">
        <el-card class="box-card">
          <div slot="header" class="clearfix">
            <span slot="label" style="float: left;margin-top: -10px;color: red;"><i class="el-icon-s-flag"></i> 热销楼盘</span>
          </div>
          <div class="card2">
            <el-row >
              <el-col :span="24" v-for="(o, index) in 7" :key="o" >
                <el-card class="card" :body-style="{ padding: '0px' }">
                  <div style="padding: 5px;display: flex">
                    <div style="width: 40%;height: 60px">
                      <img style="height: 90%;width: 90%;padding: 5px" src="http://www.shoulouxx.com/images/bgyozc9.jpg"
                           class="image-tj">
                    </div>
                    <div style="width: 60%;height: 60px;font-size: 12px;text-align: center;">
                      <span style="font-weight: bold;">龙湖时代上城</span>
                      <br>
                      <el-tag size="mini" type="danger">在售</el-tag>
                      <span>2900元</span>
                    </div>
                  </div>
                </el-card>
              </el-col>
            </el-row>
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
    name: "Layer_2nd",
    components:{
      EstateTable,
      EstateForm
    },
    computed: {
      classOption () {
        return {
          step: 0.25,
          limitMoveNum: 1,//这个是修改moveSwitch()之前的使用方法，这里的数值指的是数据条数
          openTouch: false,
        }
      }
    },
    data () {
      return {
        listData: [{
          'house': '龙湖时代上城',
          'price': '29000元/㎡'
        }, {
          'house': '碧桂园欧洲城',
          'price': '6600元/㎡'
        }, {
          'house': '明发江湾新城',
          'price': '6500元/㎡'
        }, {
          'house': '世茂·璀璨江山',
          'price': '24500元/㎡'
        }, {
          'house': '世贸璀璨睿湾',
          'price': '29000元/㎡'
        }, {
          'house': '碧桂园凤凰城',
          'price': '8600元/㎡'
        }, {
          'house': '明发江湾新城',
          'price': '9000元/㎡'
        }, {
          'house': '恒大养生谷',
          'price': '5000元/㎡'
        }, {
          'house': '电建洺悦华府',
          'price': '28000元/㎡'
        }, {
          'house': '银城旭辉云台天境',
          'price': '31000元/㎡'
        }]
      }
    }
  }
</script>

<style scoped>
  .row-bg2{
    padding-top: 20px;
  }
  .row-left{
    width: 100%;
  }
  .row-left>>> .el-col-1 {
    width: 10%;
  }
  .row-left>>> .el-col-2 {
    width: 20%;
  }
  .row-left>>> .el-col-7 {
    width: 70%;
  }



  .third-content-right>>> .el-card__body {
    padding: 3px;
  }
  .third-content-right>>> .el-card__header{
    height: 60px;
  }
</style>
