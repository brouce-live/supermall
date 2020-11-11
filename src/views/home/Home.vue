<template>
  <div id="home">
    <nav-bar class="home-nav">
      <div slot="center">购物街</div>
    </nav-bar>
    <home-carousel :banner="banner"></home-carousel>
    <recommend-view :banner="banner"></recommend-view>
  </div>
</template>

<script>
import NavBar from "@/components/common/navbar/NavBar";
import HomeCarousel from "@/views/home/childShow/HomeCarousel";
import RecommendView from "@/views/home/childShow/RecommendView";
import {getHomeMultidata} from "@/network/home";

export default {
  name: "Home",
  components: {
    NavBar,
    HomeCarousel,
    RecommendView
  },
  data(){
    return{
      banner: []
    }
  },
  created() {
    getHomeMultidata().then(res => {
      this.banner = res.data.banner.list;
    })
  }
}
</script>

<style scoped>
.home-nav{
  background-color: pink;
  color: white;
}
</style>
