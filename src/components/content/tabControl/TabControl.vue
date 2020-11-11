<template>
<div class="tab-control">
  <el-tabs v-model="activeName" @tab-click="handleClick" style="margin-left: 10px">
    <el-tab-pane label="流行" name="first">流行</el-tab-pane>
    <el-tab-pane label="新款" name="second">新款</el-tab-pane>
    <el-tab-pane label="精选" name="third">精选</el-tab-pane>
  </el-tabs>
</div>
</template>

<script>
export default {
  name: "TabControl",
  data() {
    return {
      activeName: 'second'
    };
  },
  methods: {
    handleClick(tab, event) {
      console.log(tab, event);
    }
  }
}
</script>

<style scoped>
.tab-control{
  text-align: center;
}
</style>
