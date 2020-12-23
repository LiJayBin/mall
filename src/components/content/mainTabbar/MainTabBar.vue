<template>
  <tab-bar>
      <tab-baritem path="/home">
        <img slot="item-icon" src="~assets/img/tabbar/home.png" alt="">
        <div slot="item-text">首页</div>
        <img slot="item-icon-active" src="~assets/img/tabbar/home-o.png" alt="">
      </tab-baritem>
      <tab-baritem path="/categroy" activeColor="blue">
        <img slot="item-icon" src="~assets/img/tabbar/category.png" alt="">
        <div slot="item-text">分类</div>
        <img slot="item-icon-active" src="~assets/img/tabbar/category-o.png" alt="">
      </tab-baritem>
      <tab-baritem path="/cart">
        <img slot="item-icon" src="~assets/img/tabbar/cart.png" alt="">
        <div slot="item-text">购物车</div>
        <img slot="item-icon-active" src="~assets/img/tabbar/cart-o.png" alt="">
      </tab-baritem>
      <tab-baritem path="/profile">
        <img slot="item-icon" src="~assets/img/tabbar/my.png" alt="">
        <div slot="item-text">我的</div>
        <img slot="item-icon-active" src="~assets/img/tabbar/my-o.png" alt="">
      </tab-baritem>
  </tab-bar>
</template>

<script>
import TabBar from 'common/tabbar/TabBar';
import TabBaritem from 'common/tabbar/TabBaritem.vue'

export default {
    name:'MainTabBar',
    components:{
        TabBar,
        TabBaritem
    }
}
</script>

<style>

</style>