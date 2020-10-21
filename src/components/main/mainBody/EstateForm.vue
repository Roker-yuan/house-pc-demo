<template>
  <el-form ref="form" :model="form"  class="my-form">
    <!--地区-->
    <el-form-item>
      <el-select v-model="form.region" size="mini" placeholder="六合区">
        <el-option label="六合区" value="shanghai" ></el-option>
        <el-option label="区域二" value="beijing"></el-option>
      </el-select>
    </el-form-item>
   <!--价位-->
    <el-form-item>
      <el-select v-model="form.region" size="mini" placeholder="40-100万">
        <el-option label="六合区" value="shanghai" ></el-option>
        <el-option label="区域二" value="beijing"></el-option>
      </el-select>
    </el-form-item>
    <!--格局-->
    <el-form-item>
      <el-select v-model="form.region" size="mini" placeholder="一居室">
        <el-option label="六合区" value="shanghai" ></el-option>
        <el-option label="区域二" value="beijing"></el-option>
      </el-select>
    </el-form-item>
    <!--服务承诺-->
    <el-form-item>
      <el-select v-model="form.region" size="mini" placeholder="买贵包赔">
        <el-option label="六合区" value="shanghai" ></el-option>
        <el-option label="区域二" value="beijing"></el-option>
      </el-select>
    </el-form-item>
    <!--姓名-->
    <el-form-item style="margin-left: 25px;margin-right: 25px">
      <el-input v-model="form.name" size="mini" placeholder="姓名"></el-input>
    </el-form-item>
    <!--电话-->
    <el-form-item style="margin-left: 25px;margin-right: 25px">
      <el-input v-model="form.name" size="mini" placeholder="电话"></el-input>
    </el-form-item>
    <!--要求-->
    <el-form-item style="margin-left: 25px;margin-right: 25px">
      <el-input type="textarea" size="mini" v-model="form.desc" placeholder="对楼盘和户型还有什么要求"></el-input>
    </el-form-item>
    <div style="margin-bottom: 15px;margin-top: 20px;font-size: small">
      已帮助<span style="font-size: small;color: red">996</span>位客户成功购房
    </div>
    <el-form-item>
      <el-button type="danger" round size="mini" @click="onSubmit">提交申请</el-button>
    </el-form-item>
      <div class="nr" style="margin-bottom: 25px;margin-top: 10px;font-size: small">
        <span style="font-size: large;color: red">帮你优质选房</span><br>
        留下需求，为您挑选最满意的房源
      </div>
  </el-form>
</template>

<script>
    export default {
        name: "EstateForm",
      data() {
        return {
          form: {
            name: '',
            region: '',
            date1: '',
            date2: '',
            delivery: false,
            type: [],
            resource: '',
            desc: ''
          }
        }
      },
      methods: {
        onSubmit() {
          console.log('submit!');
        }
      }
    }
</script>

<style scoped>
  .my-form>>>.el-form-item {
     margin-bottom: 0px;
  }
</style>
