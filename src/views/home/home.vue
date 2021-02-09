<template>
  <div id="home">
    <nav-bar class="home-nav">
      <div slot="nav-center">购物车</div>
    </nav-bar>
    <home-swiper :banners="banners" />
    <home-recommend :recommends="recommends" />
  </div>
</template>

<script>
import NavBar from "components/common/navbar/NavBar";
import {getHomeMulitData} from "network/home";
import HomeSwiper from "./childComp/HomeSwiper";
import HomeRecommend from "./childComp/HomeRecommend";

export default {
  name: "home",
  components: {
    NavBar,
    HomeSwiper,
    HomeRecommend
  },
  data() {
    return {
      banners: [],
      recommends: [],
    }
  },
  created() {
    getHomeMulitData()
    .then(res => {
      // console.log(res);
      this.banners = res.data.data.banner.list;
      this.recommends = res.data.data.recommend.list;
    })
  }
}
</script>

<style scoped>

#home {
  position: relative;
  height: 100vh;
  width: 100%;
}

.home-nav {
  color: #FFFFFF;
  background-color: deeppink;
}

</style>
