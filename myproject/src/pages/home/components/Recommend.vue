<template>
   <div>
      <div class="recommend-title">热销推荐</div>
      <ul>
        <li class="item  border-bottom" v-for="(item,index) of recommendList" :key="index">
                <img class="item-img" :src="item.imgUrl">
            <div class="item-info">
                <p class="item-tiyle">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
                <button class="item-button">查看详情</button>
            </div>
        </li>
      </ul>
   </div>
</template>
<script>
export default {
    name:"HomeRecommend",
    data (){
        return {
            recommendList:[{
                id:"0001",
                imgUrl:"http://img1.qunarzz.com/sight/p0/201403/10/b0e7eeb18db9a7dc4f0376a13d4ab15d.jpg_200x200_3ff00ade.jpg",
                title:"关中民俗艺术博物院",
                desc:"关中民俗艺术博物院成人票（赠古风团扇）关中民俗艺术博物院成人票（赠古风团扇）"
            },{
                id:"0002",
                imgUrl:"http://img1.qunarzz.com/sight/p0/201403/10/b0e7eeb18db9a7dc4f0376a13d4ab15d.jpg_200x200_3ff00ade.jpg",
                title:"关中民俗艺术博物院",
                desc:"关中民俗艺术博物院成人票（赠古风团扇）关中民俗艺术博物院成人票（赠古风团扇）"
            },{
                id:"0003",
                imgUrl:"http://img1.qunarzz.com/sight/p0/201403/10/b0e7eeb18db9a7dc4f0376a13d4ab15d.jpg_200x200_3ff00ade.jpg",
                title:"关中民俗艺术博物院",
                desc:"关中民俗艺术博物院成人票（赠古风团扇）关中民俗艺术博物院成人票（赠古风团扇）"
            },
            ]
        }
    }
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl'
  .recommend-title
    line-height:.8rem
    background :#eee
    text-indent:.2rem
   .item
    display:flex
    height 1.9rem
    overflow:hidden
    .item-img
     width:1.7rem
     height 1.7rem
     padding:0.1rem
    .item-info
     flex:1
     min-width:0
     padding:.1rem
    .item-title
     line-height:.54rem
     font-size:.32rem
     ellipsis()
    .item-desc
     line-height:.4rem
     color:#ccc
     ellipsis()
    .item-button
     line-height:.44rem
     margin-top:.16rem
     background #ff9300
     padding:0 .2rem
     border-radius:.06rem 
     color:#fff
</style>
