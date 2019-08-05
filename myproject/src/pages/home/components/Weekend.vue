<template>
   <div>
      <div class="recommend-title">周末去哪儿</div>
      <ul>
        <li class="item  border-bottom" v-for="(item,index) of recommendList" :key="index">
               <div class="item-img-wrapper">
                    <img class="item-img" :src="item.imgUrl">
               </div>
            <div class="item-info">
                <p class="item-tiyle">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
                
            </div>
        </li>
      </ul>
   </div>
</template>
<script>
export default {
    name:"HomeWeekend",
    data (){
        return {
            recommendList:[{
                id:"0001",
                imgUrl:"http://img1.qunarzz.com/sight/source/1507/fe/679926851c309a.jpg_r_640x214_114816de.jpg",
                title:"关中民俗艺术博物院",
                desc:"关中民俗艺术博物院成人票（赠古风团扇）关中民俗艺术博物院成人票（赠古风团扇）"
            },{
                id:"0002",
                imgUrl:"http://img1.qunarzz.com/sight/source/1511/14/1cf5dc2ecbfc16.jpg_r_640x214_b4b3a58a.jpg",
                title:"关中民俗艺术博物院",
                desc:"关中民俗艺术博物院成人票（赠古风团扇）关中民俗艺术博物院成人票（赠古风团扇）"
            },{
                id:"0003",
                imgUrl:"http://img1.qunarzz.com/sight/source/1507/de/e6ba44d61894c0.jpg_r_640x214_847324d0.jpg",
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
    margin-top:.2rem
.item-img-wrapper
 overflow:hidden
 height:0
 padding-bottom:33.9%
 .item-img
  width:100% 
.item-info
 padding:.1rem
 .item-title
   line-height:.54rem
   font-size:.32rem
   ellipsis()
 .item-desc
  line-height:.4rem
  color:#ccc
  ellipsis()

</style>
