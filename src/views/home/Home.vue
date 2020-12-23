<template>
  <div id="Home">
    <nav-bar class="nav-bar"><div slot="center">购物街</div></nav-bar>
    <home-swiper :banners="banners"></home-swiper>
    <home-recommend-view :recommends="recommends"></home-recommend-view>
  </div>
</template>

<script>
import NavBar from 'components/common/navbar/NavBar.vue'
import HomeSwiper from './childComps/HomeSwiper'
import HomeRecommendView from './childComps/HomeRecommendView.vue'
import {getHomeMultidata} from 'network/home'

export default {
  name:'Home',
  data(){
    return{
      // result:null,
      banners:[],
      recommends:[]
    }
  },
  components: {
    NavBar,
    HomeSwiper,
    HomeRecommendView
  },
  created(){
    getHomeMultidata().then(res => {
      // console.log(res)
      // this.result = res;
      this.banners = res.data.banner.list;
      this.recommends = res.data.recommend.list;
    })
    // console.log(this.result)
  }
}
</script>

<style>
 .nav-bar {
    background-color: var(--color-tint);
    font-weight: 700;
    color: #fff;
  }
</style>