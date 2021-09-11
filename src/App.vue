<template>
  <div id="app">
    <main-tab-bar></main-tab-bar>
  </div>
  <router-view/>
</template>

<script>
  import MainTabBar from "components/content/mainTabbar/MainTabBar";

  export default {
    name: 'app',
    components: {
      MainTabBar
    }
  }
</script>

<style>
  @import "assets/css/base.css";
  @import "assets/css/normalize.css";
</style>
