<template>
  <div id="app">
    <router-view />
    <TabBar>
      <TabBarItem path='/home'>
        <img src="./assets/img/tabbar/home.svg" alt="" slot="item-icon">
        <img src="./assets/img/tabbar/home_active.svg" alt="" slot="item-icon-active">
        <div slot="item-text">首页</div>
      </TabBarItem>
      <TabBarItem path='/category'>
        <img src="./assets/img/tabbar/category.svg" alt="" slot="item-icon">
        <img src="./assets/img/tabbar/category_active.svg" alt="" slot="item-icon-active">
        <div slot="item-text">分类</div>
      </TabBarItem>
      <TabBarItem path='/cart'>
        <img src="./assets/img/tabbar/cart.svg" alt="" slot="item-icon">
        <img src="./assets/img/tabbar/cart_active.svg" alt="" slot="item-icon-active">
        <div slot="item-text">购物车</div>
      </TabBarItem>
      <TabBarItem path='/profile'>
        <img src="./assets/img/tabbar/profile.svg" alt="" slot="item-icon">
        <img src="./assets/img/tabbar/profile_active.svg" alt="" slot="item-icon-active">
        <div slot="item-text">我的</div>
      </TabBarItem>
    </TabBar>
  </div>
</template>

<script>
import TabBar from './components/tabbar/TabBar'
import TabBarItem from './components/tabbar/TabBarItem'
export default {
  name: 'App',
  components: {
    TabBar,
    TabBarItem
  }
}
</script>

<style>
@import './assets/css/basic.css';
.color {
  color: #d81e06;
}
</style>
