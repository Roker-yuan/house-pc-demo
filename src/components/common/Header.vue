<template>
  <el-row>
    <el-col :span="8">
      <div class="grid-content bg-purple">
        <img class="header_img" src="@/assets/headerLogo.png">
      </div>
    </el-col>
  </el-row>
</template>

<script>
    export default {
        name: "Header"
    }
</script>

<style scoped>
  .bg-purple {
    background: rgba(211, 220, 230, 0.01);
  }
  .grid-content {
    border-radius: 4px;
    min-height: 100%;
  }
  .header_img{
    height: 40px;
    margin: 10px;
    float: right;
  }

</style>
