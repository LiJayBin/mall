<template>
  <div id="profile">
    <nav-bar class="nav-bar"><div slot="center">俊博商城</div></nav-bar>
  </div>
</template>

<script>
import NavBar from 'components/common/navbar/NavBar'

export default {
  name:'profile',
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