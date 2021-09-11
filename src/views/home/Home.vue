<template>
  <div id="home">
    <nav-bar class="home-nav">
      <template v-slot:center>
        <div>购物车</div>
      </template>
    </nav-bar>
    <div id="hy-swiper">
      <div class="swiper">
        <div class="swiper-item" v-for="item in banners">
          <a :href="item.link">
            <img :src="item.image" alt="">
          </a>
        </div>
      </div>
      <div class="indicator">

      </div>
    </div>
    <recommend-view :recommends="recommends"></recommend-view>
    <feature-view></feature-view>
    <tab-control class="tab-control"
                :titles="['流行', '新款', '精选']">
    </tab-control>
    <ul>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
      <li>111</li>
    </ul>
  </div>
</template>

<script>
import RecommendView from "./childComps/RecommendView";
import FeatureView from "./childComps/FeatureView";

import NavBar from "../../components/common/navbar/NavBar";
import TabControl from "../../components/content/tabControl/TabControl";

import { getHomeMultidata } from "../../network/home";


export default {
  name: "Home",
  components: {
    RecommendView,
    FeatureView,
    NavBar,
    TabControl
  },
  data() {
    return {
      banners: [],
      recommends: [],
      slideCount: 0,  // 元素个数
      totalWidth: 0,  // swiper的宽度
      swiperStyle: {}, // swiper样式
      currentIndex: 1, // 当前的index
      scrolling: false, // 是否正在滚动
    }
  },
  created() {
    this.getHomeMultidata()
  },
  methods: {
    getHomeMultidata() {
      getHomeMultidata().then(res => {
        this.banners = res.data.banner.list;
        this.recommends = res.data.recommend.list;
      })
    },

  }
}
</script>

<style scoped>
  #home {
    margin-top: 44px;
  }
  .home-nav {
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
    z-index: 9;

    background-color: var(--color-tint);
  }

  #hy-swiper {
    overflow: hidden;
    position: relative;
  }
  .swiper {
    display: flex;
  }
  .swiper-item {
    width: 100%;
    flex-shrink: 0;
  }
  .swiper-item img {
    width: 100%;
    height: 170px;
  }

  .tab-control {
    position: sticky;
    top: 44px;
    z-index: 9;
  }
</style>