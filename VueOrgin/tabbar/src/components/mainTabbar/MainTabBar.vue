<template>
  <tab-bar>
    <tar-bar-item path="/home" activeColor="brown">
      <img slot="item_icon" src="~assets/img/tabbar/home.svg" alt="">
      <img slot="item_icon_active" src="~assets/img/tabbar/home_active.svg" alt="">
      <div slot="item_text">首页</div>
    </tar-bar-item>
    <tar-bar-item path="/category" activeColor="brown">
      <img slot="item_icon" src="~assets/img/tabbar/category.svg" alt="">
      <img slot="item_icon_active" src="~assets/img/tabbar/category_active.svg" alt="">
      <div slot="item_text">分类</div>
    </tar-bar-item>
    <tar-bar-item path="/shopcart" activeColor="brown">
      <img slot="item_icon" src="~assets/img/tabbar/shopcart.svg" alt="">
      <img slot="item_icon_active" src="~assets/img/tabbar/shopcart_active.svg" alt="">
      <div slot="item_text">购物车</div>
    </tar-bar-item>
    <tar-bar-item path="profile" activeColor="brown">
      <img slot="item_icon" src="~assets/img/tabbar/profile.svg" alt="">
      <img slot="item_icon_active" src="~assets/img/tabbar/profile_active.svg" alt="">
      <div slot="item_text">我的</div>
    </tar-bar-item>
  </tab-bar>
</template>

<script>
  import TabBar from "components/tabbar/TabBar";
  import TarBarItem from "components/tabbar/TarBarItem";

  export default {
    name: "MainTabBar",
    components: {
      TabBar,
      TarBarItem
    }
  }

</script>

<style scoped>

</style>
