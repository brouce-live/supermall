<template>
<div class="recommend">
  <div v-for="item in banner" class="recommend-item">
    <a :href="item.link">
      <el-avatar :src="item.image" :size="70"></el-avatar>
    </a>
    <div>{{item.title}}</div>
  </div>
</div>
</template>

<script>
export default {
name: "RecommendView",
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
.recommend{
  display: flex;
  width: 100%;
  text-align: center;
  font-size: 12px;
  padding: 5px 0 20px;
  border-bottom: 8px solid #eee;
}
.recommend-item{
  flex: 1;
}

</style>
