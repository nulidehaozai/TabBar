<template>
    <div id="tab-bar">
    <div class="tab-bar-item" @click = "see1 = !see1">
        <img  v-if="see1" src="../../assets/img/tabbar/home.svg">
        <img  v-else src="../../assets/img/tabbar/home_active.svg">         
        <div :class={active:!see1}>首页</div>
        </div>
    <div class="tab-bar-item"  @click = "see2 = !see2">
        <img v-if="see2" src="../../assets/img/tabbar/category.svg">
        <img v-else src="../../assets/img/tabbar/category_active.svg"> 
        <div :class={active:!see2}>分类</div>
        </div>
    <div class="tab-bar-item"  @click = "see3 = !see3">
        <img v-if="see3" src="../../assets/img/tabbar/shopcart.svg">
        <img v-else src="../../assets/img/tabbar/shopcart_active.svg"> 
        <div :class={active:!see3}>购物车</div>
        </div>
    <div class="tab-bar-item"  @click = "see4 = !see4">
        <img v-if="see4" src="../../assets/img/tabbar/profile.svg">
        <img v-else src="../../assets/img/tabbar/profile_active.svg"> 
        <div :class={active:!see4}>我的</div>
        </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            see1 : true,
            see2 : true,
            see3 : true,
            see4 : true
        }
    }

};
</script>

<style scoped>
#tab-bar {
  display: flex; 
  background-color: #f6f6f6;
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  box-shadow: 0 -3px 1px rgba(100,100,100,.1);
}

.tab-bar-item {
  flex: 1;
  height: 49px;
  text-align: center;
}
.tab-bar-item  img{
    width: 100%;
    height: 24px;
}
.active{
    color: #FF5777;
}
</style>