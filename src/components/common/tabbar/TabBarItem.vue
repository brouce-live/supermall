<template>
<div class="tab-bar-item" @click="itemClick">
  <div v-if="!isActive"><slot name="item-icon"></slot></div>
  <div v-else><slot name="item-icon_active"></slot></div>
  <div v-bind:class="{active: isActive}"><slot name="item-text"></slot></div>
<!--  <img src="../../assets/img/tabbar/home.svg" alt="首页" />-->
<!--  <div>首页</div>-->
</div>
</template>

<script>
export default {
  name: "TabBarItem",
  props:{
    path: String
  },
  data() {
    return{
      //isActive: false
    }
  },
  computed: {
    isActive(){
      return this.$route.path.indexOf(this.path) !== -1
    }
  },
  methods: {
    itemClick(){
      this.$router.replace(this.path)
      // console.log("itemClick");
    }
  }
}
</script>

<style scoped>
@import "../../../assets/css/base.css";
</style>
