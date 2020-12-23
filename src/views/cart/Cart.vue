<template>
  <div id="cart">
    <nav-bar class="nav-bar"><div slot="center">购物车</div></nav-bar>
  </div>
</template>

<script>
import NavBar from 'components/common/navbar/NavBar'

export default {
  name:'cart',
  components:{
    NavBar,
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