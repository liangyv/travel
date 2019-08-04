<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
    <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" alt="">
    </swiper-slide>
   
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
    </div>
</template>
<script>
export default {
    name:"HomeSwiper",
    data (){
        return {
            swiperOption:{
                pagination:'.swiper-pagination',
                loop:true
            },
            swiperList:[{
                id:"0001",
                imgUrl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20198/e13be43d0f309c205d9f51113778e41a.jpg_890x330_8f70f900.jpg'},
                {
                 id:"0002",
                imgUrl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/96f5d3dbdec9c84c25576c9ad6d9712a.jpg_890x330_7c4ba2a0.jpg'   
                }
                ]
        }
    }
    
}
</script>
<style lang="stylus" scoped>
.wrapper>>> .swiper-pagination-bullet-active
        background :red !important
.wrapper
    width:100%
    height:0
    overflow:hidden
    padding-bottom:31.25%    
    .swiper-img
        width:100%
</style>
