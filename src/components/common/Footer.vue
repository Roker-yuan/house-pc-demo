<template>
  <div class="footer" style="color: white;">
    <el-link  :underline="false">Copyright © 2001-2020  |</el-link>
    <el-link :underline="false">ROKER TERM   |</el-link>
    <el-link :underline="false">联系方式</el-link>
  </div>
</template>

<script>
    export default {
        name: "Footer"
    }
</script>

<style scoped>
  .footer>>> .el-link.el-link--default {
    color: white;
  }
</style>
