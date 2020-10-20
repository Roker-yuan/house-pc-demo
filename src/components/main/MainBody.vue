<template>
    <div>
      <div>
        <Carousel></Carousel>
      </div>
      <div>
        <Layer_1st></Layer_1st>
      </div>
      <div>
        <Layer_2nd></Layer_2nd>
      </div>
      <div>
        <Layer_3rd></Layer_3rd>
      </div>



    </div>
</template>

<script>
    import Carousel from "../rotation/Carousel";
    import Layer_1st from "../main/mainBody/Layer_1st";
    import Layer_2nd from "../main/mainBody/Layer_2nd";
    import Layer_3rd from "../main/mainBody/Layer_3rd";
    export default {
        name: "MainBody",
        components:{
          Carousel,
          Layer_1st,
          Layer_2nd,
          Layer_3rd
        }
    }

</script>

<style scoped>

</style>
