<template>
  <el-carousel :interval="4000" type="card" height="200px">
    <el-carousel-item v-for="item in banner">
      <a :href="item.link">
        <img :src="item.image" alt="" style="height: 200px">
      </a>
    </el-carousel-item>
  </el-carousel>
</template>

<script>
export default {
  name: "HomeCarousel",
  props:{
    banner:{
      type: Array,
      default(){
        return []
      }
    }
  }
}
</script>

<style scoped>

</style>
