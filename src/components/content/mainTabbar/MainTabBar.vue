<template>
  <div>
    <tab-bar>
      <tab-bar-item path="/home" activeColor="blue">
        <template v-slot:item-icon>
          <img src="~assets/img/home.svg" style="width: 24px;height: 24px;" alt="">
        </template>
        <template v-slot:item-icon-active>
          <img src="~assets/img/home-active.svg" style="width: 24px;height: 24px;" alt="">
        </template>
        <template v-slot:item-text>
          <div>首页</div>
        </template>
      </tab-bar-item>
      <tab-bar-item path="/category" activeColor="blue">
        <template v-slot:item-icon>
          <img src="~assets/img/home.svg" style="width: 24px;height: 24px;" alt="">
        </template>
        <template v-slot:item-icon-active>
          <img src="~assets/img/home-active.svg" style="width: 24px;height: 24px;" alt="">
        </template>
        <template v-slot:item-text>
          <div>分类</div>
        </template>
      </tab-bar-item>
      <tab-bar-item path="/cart" activeColor="blue">
        <template v-slot:item-icon>
          <img src="~assets/img/home.svg" style="width: 24px;height: 24px;" alt="">
        </template>
        <template v-slot:item-icon-active>
          <img src="~assets/img/home-active.svg" style="width: 24px;height: 24px;" alt="">
        </template>
        <template v-slot:item-text>
          <div>购物车</div>
        </template>
      </tab-bar-item>
      <tab-bar-item path="/profile" activeColor="blue">
        <template v-slot:item-icon>
          <img src="~assets/img/home.svg" style="width: 24px;height: 24px;" alt="">
        </template>
        <template v-slot:item-icon-active>
          <img src="~assets/img/home-active.svg" style="width: 24px;height: 24px;" alt="">
        </template>
        <template v-slot:item-text>
          <div>我的</div>
        </template>
      </tab-bar-item>
    </tab-bar>
  </div>
</template>

<script>
import TabBar from "../../common/tabbar/TabBar";
import TabBarItem from "../../common/tabbar/TabBarItem";

export default {
  name: "MainTabBar",
  components: {
    TabBar,
    TabBarItem
  }
}
</script>

<style scoped>

</style>
