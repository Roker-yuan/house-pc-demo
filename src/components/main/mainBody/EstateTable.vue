<template>
  <div class="estate-t">
    <el-table border style="width: 100%"
              :data="tableData"
              :span="24"
              cell-class-name="cellClassName"
              header-cell-class-name="headerCellClassName"
              :cell-style="cellStyle"
    >
      <el-table-column prop="name" label="楼盘名称" width="130"> </el-table-column>
      <el-table-column prop="address" label="地址" width="280"> </el-table-column>
      <el-table-column prop="area" label="区域" width="80"> </el-table-column>
      <el-table-column prop="price" label="单价" width="80"> </el-table-column>
      <el-table-column prop="preferential" label="特惠" width="180" > </el-table-column>
      <el-table-column prop="state" label="状态" width="60"> </el-table-column>
      <el-table-column prop="consult" label="咨询"  width="65"> </el-table-column>
    </el-table>
  </div>

</template>

<script>
    export default {
        name: "EstateTable",
      data(){
          return{
            tableData: [{
              name: '碧桂园凤凰城',
              address: '句容市黄梅镇黄龙路与汤山S122出口交汇处',
              area: '句容市',
              price: '8500',
              preferential: '具体优惠请致电售楼部',
              state: '在售',
              consult: '咨询'
            }, {
              name: '碧桂园欧洲城',
              address: '安徽省滁州市南谯区滁宁快速通道南侧',
              area: '滁州市',
              price: '6600',
              preferential: '具体优惠请致电售楼部',
              state: '在售',
              consult: '咨询'
            }, {
              name: '电建洺悦华府',
              address: '岱山东路与岱山北路交界处向东300米',
              area: '南京市',
              price: '28000',
              preferential: '具体优惠请致电售楼部',
              state: '在售',
              consult: '咨询'
            }, {
              name: '恒大养生谷',
              address: '南京江北新区金牛湖地铁站东侧',
              area: '浦口区',
              price: '12800',
              preferential: '具体优惠请致电售楼部',
              state: '在售',
              consult: '咨询'
            }, {
              name: '金隅紫京叠院',
              address: '江北新区黄山岭路与狮山路交汇处',
              area: '江北新区',
              price: '29000',
              preferential: '具体优惠请致电售楼部',
              state: '在售',
              consult: '咨询'
            }, {
              name: '句容恒大文化旅游城',
              address: '句容市宝华山路和容城大道交叉口',
              area: '句容市',
              price: '9000',
              preferential: '具体优惠请致电售楼部',
              state: '在售',
              consult: '咨询'
            }]
          }
      },
      methods: {
        cellStyle(row,column,rowIndex,columnIndex){//根据报警级别显示颜色
          // console.log(row);
          // console.log(row.column);
          if(row.column.label==="特惠"){
            return 'color:red'
          }
          if(row.column.label==="咨询"){
            return 'color:red'
          }
        }
      }
    }
</script>

<style scoped>

  .estate-t>>>.el-table .headerCellClassName {
    color: #0a0a0a;
    background-color: #ddd;
    font-weight: 100;
    font-size: x-small;
    text-align: center;
    line-height: 10px;
  }
   .estate-t>>>.el-table .cellClassName {
     color: #0a0a0a;
     background-color: #ffffff;
     font-weight: 100;
     font-size: smaller;
     text-align: center;
     min-height: 10px;
   }
  .estate-t >>> .el-table td, .el-table th {
    padding: 0px 0;
    min-width: 0;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    text-overflow: ellipsis;
    vertical-align: middle;
    position: relative;

  }
  .estate-t>>>.el-table__header tr,.el-table__header th {
    padding: 0;
    height: 10px;
  }
  .estate-t>>>.el-table__body tr,.el-table__body td {
    padding: 0;
    height: 40px;
  }
</style>
