<template>
  <div class="tab-bar-item" @click="itemClick">
      <div v-if="!isActive"><slot name="item-icon"></slot></div>
      <div v-else><slot name="item-icon-active"></slot></div>
      <!-- <div :class="{active:isActive}"> <slot name="item-text"></slot></div> -->
      <div :style="activeStyle"> <slot name="item-text"></slot></div>
  </div>
</template>

<script>
export default {
    name:'TabBaritem',
    props:{
        path:String,
        activeColor:{
            type:String,
            default:'rgb( 255, 45, 74)',
        }
    },
    data(){
        return{
            // 写死就不变了isActive:true,
            // path:'/home' path不能写死，从父传子拿到path值，这里在app.vue中path
            // 原封不动拿过来，就不用写成:path
        }
    },
    computed:{
        isActive(){
            //返回时检查，当前活跃路由的path跟传递过来的path /home->item1(/home)=true
            return this.$route.path.indexOf(this.path) !== -1
        },
        activeStyle(){
            return this.isActive ? {color:this.activeColor} : {}
        }
    },
    methods:{
        itemClick(){
            this.$router.replace(this.path)
        }
    }
}
</script>

<style>
 .tab-bar-item{
   flex: 1;
   text-align: center;
   align-items: center;
   justify-content: center;
   height: 49px;
   font-size: 14px;
 }
 .tab-bar-item img{
     width: 24px;
     height: 24px;
     margin-top: 3px;
     vertical-align: middle;
     margin-bottom: 2px;
 }
 /*颜色不写死，方便后期修改 
  .active{
     color:rgb( 255, 45, 74);
 } */
</style>