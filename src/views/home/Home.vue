<template>
  <div id="home">
    <nav-bar class="home-nav">
      <div slot="center">购物街</div>
    </nav-bar>
    <home-carousel :banner="banner"></home-carousel>
    <recommend-view :banner="banner"></recommend-view>
    <feature-view></feature-view>
    <tab-control></tab-control>
    <ul>
      <li>待开发1</li>
      <li>待开发2</li>
      <li>待开发3</li>
      <li>待开发4</li>
      <li>待开发5</li>
      <li>待开发6</li>
      <li>待开发7</li>
      <li>待开发8</li>
      <li>待开发9</li>
      <li>待开发10</li>
      <li>待开发11</li>
      <li>待开发12</li>
      <li>待开发13</li>
      <li>待开发14</li>
      <li>待开发15</li>
      <li>待开发16</li>
      <li>待开发17</li>
      <li>待开发18</li>
      <li>待开发19</li>
      <li>待开发20</li>
      <li>待开发21</li>
      <li>待开发22</li>
      <li>待开发23</li>
      <li>待开发24</li>
      <li>待开发25</li>
      <li>待开发26</li>
      <li>待开发27</li>
      <li>待开发28</li>
      <li>待开发29</li>
      <li>待开发30</li>
      <li>待开发31</li>
      <li>待开发32</li>
      <li>待开发33</li>
      <li>待开发34</li>
      <li>待开发35</li>
      <li>待开发36</li>
      <li>待开发37</li>
      <li>待开发38</li>
      <li>待开发39</li>
      <li>待开发40</li>
      <li>待开发41</li>
      <li>待开发42</li>
      <li>待开发43</li>
      <li>待开发44</li>
      <li>待开发45</li>
      <li>待开发46</li>
      <li>待开发47</li>
      <li>待开发48</li>
      <li>待开发49</li>
      <li>待开发50</li>
      <li>待开发51</li>
      <li>待开发52</li>
      <li>待开发53</li>
      <li>待开发54</li>
      <li>待开发55</li>
      <li>待开发56</li>
      <li>待开发57</li>
      <li>待开发58</li>
      <li>待开发59</li>
      <li>待开发60</li>
      <li>待开发61</li>
      <li>待开发62</li>
      <li>待开发63</li>
      <li>待开发64</li>
      <li>待开发65</li>
      <li>待开发66</li>
      <li>待开发67</li>
      <li>待开发68</li>
      <li>待开发69</li>
      <li>待开发70</li>
      <li>待开发71</li>
      <li>待开发72</li>
      <li>待开发73</li>
      <li>待开发74</li>
      <li>待开发75</li>
      <li>待开发76</li>
      <li>待开发77</li>
      <li>待开发78</li>
      <li>待开发79</li>
      <li>待开发80</li>
      <li>待开发81</li>
      <li>待开发82</li>
      <li>待开发83</li>
      <li>待开发84</li>
      <li>待开发85</li>
      <li>待开发86</li>
      <li>待开发87</li>
      <li>待开发88</li>
      <li>待开发89</li>
      <li>待开发90</li>
      <li>待开发91</li>
      <li>待开发92</li>
      <li>待开发93</li>
      <li>待开发94</li>
      <li>待开发95</li>
      <li>待开发96</li>
      <li>待开发97</li>
      <li>待开发98</li>
      <li>待开发99</li>
      <li>待开发100</li>
    </ul>
  </div>
</template>

<script>
import NavBar from "@/components/common/navbar/NavBar";
import TabControl from "@/components/content/tabControl/TabControl";

import HomeCarousel from "@/views/home/childShow/HomeCarousel";
import RecommendView from "@/views/home/childShow/RecommendView";
import FeatureView from "@/views/home/childShow/FeatureView";

import {getHomeMultidata} from "@/network/home";

export default {
  name: "Home",
  components: {
    NavBar,
    HomeCarousel,
    RecommendView,
    FeatureView,
    TabControl
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
#home{
  padding-top: 44px;
}
.home-nav{
  background-color: pink;
  color: white;
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  z-index: 9;
}
</style>
