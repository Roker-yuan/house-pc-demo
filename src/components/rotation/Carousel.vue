<template>
  <div class="c-body" style="text-align: center">
    <div class="c-image" style="position:sticky;">
      <el-carousel :interval="5000" arrow="always" height="500px">
        <el-carousel-item v-for="item in carouselImgs.images" :key="item.name">
          <img style="width:100%;height:100%;" :src="item.url" />
        </el-carousel-item>
      </el-carousel>
    </div>
    <el-card class="box-card" style="width: 30%;position: absolute;top: 400px; left: 35%;z-index: 20;background: rgba(36, 36, 36, 0.64);">
      <div class="c-search" >
        <el-select v-model="selectValue" placeholder="请选择">
          <el-option
            v-for="item in options"
            :key="item.value"
            :label="item.label"
            :value="item.value">
          </el-option>
        </el-select>
        <el-input
          v-model="search"
          @focus="focus"
          @blur="blur"
          @keyup.enter.native="searchHandler"
          placeholder=""
        >

          <el-button slot="append" icon="el-icon-search" id="search" @click="searchHandler"></el-button>
        </el-input>
      </div>
    </el-card>

  </div>

</template>

<script>
    export default {
        name: "Carousel",
      data() {
        return {
          selectValue:'4',
          activeName: '1',
          calendarValue: new Date(),
          carouselImgs: {
            images: [
              {
                name: 'carousel01',
                url: require('../../images/carousel/banner1.jpg')
              },
              {
                name: 'carousel02',
                url: require('../../images/carousel/banner2.jpg')
              },
              {
                name: 'carousel03',
                url: require('../../images/carousel/banner3.jpg')
              }
            ]
          },
          options: [{
            value: '1',
            label: '黄糕'
          }, {
            value: '2',
            label: '双奶'
          }, {
            value: '3',
            label: '蚵煎'
          }, {
            value: '4',
            label: '不限'
          }]
        }
      },
    }
</script>

<style scoped>
  .el-carousel__item h3 {
    color: #475669;
    font-size: 18px;
    opacity: 0.75;
    line-height: 300px;
    margin: 0;
  }

  .el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
  }

  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
  }

  .c-search>>> .el-select {
    display: inline-block;
    position: relative;
    width: 15%;
  }
  .c-search>>> .el-input__inner {
    padding: 0 5px;
  }

  .c-search>>> .el-input-group {
    line-height: normal;
    display: inline-table;
    width: 65%;
    border-collapse: separate;
    border-spacing: 0;
  }
  .c-search>>> .el-popper[x-placement^=bottom] {
    margin-top: 40px;
  }
</style>
