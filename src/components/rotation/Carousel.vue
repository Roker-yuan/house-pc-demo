<template>
  <el-carousel :interval="5000" arrow="always" height="500px">
<!--    <el-carousel-item v-for="item in 4" :key="item">-->
<!--      <h3>{{ item }}</h3>-->
<!--    </el-carousel-item>-->
    <el-carousel-item v-for="item in carouselImgs.images" :key="item.name">
      <!-- <h3 class="medium">{{ item }}</h3> -->
      <img style="width:100%;height:100%;" :src="item.url" />
    </el-carousel-item>
  </el-carousel>
</template>

<script>
    export default {
        name: "Carousel",
      data() {
        return {
          activeName: '1',
          calendarValue: new Date(),
          carouselImgs: {
            images: [
              {
                name: 'carousel01',
                url: require('../../images/carousel/324988.jpg')
              },
              {
                name: 'carousel02',
                url: require('../../images/carousel/banner1.jpg')
              },
              {
                name: 'carousel03',
                url: require('../../images/carousel/1000981.jpg')
              }
            ]
          }
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
</style>
