<template>
  <div>
      <div class="banner" @click="handleBannerClick"> 
          <img class="banner=img" src="//img1.qunarzz.com/sight/p0/1704/a3/a3e4f87ebd5c55a1a3.water.jpg_600x330_5ee903d6.jpg"/>
          <div class="banner-info">
              <div class="banner-title">西安幻太奇梦幻海洋馆</div>
              <div class="banner-number"><span class="iconfont back-icon">&#xe600;</span>39</div>
          </div>
      </div>
      <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
  </div>
</template>
<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
    name:'DetailBanner',
    data () {
        return{
            showGallary:false,
            imgs:['http://img1.qunarzz.com/sight/p0/1507/a4/a4af1b64e36560fd.img.jpg_r_800x800_235ea025.jpg','http://img1.qunarzz.com/sight/p0/1507/a4/a4af1b64e36560fd.img.jpg_r_800x800_235ea025.jpg']
        }
    },
    methods:{
        handleBannerClick(){
            this.showGallary=true
        },
        handleGallaryClose(){
             this.showGallary=false
        }
    },
    components:{
        CommonGallary
    }
}
</script>
<style lang="stylus" scoped>
.banner
 position :relative
 overflow:hidden
 height:0
 padding-bottom:55%
 .banner-img
  width:100%
 .banner-info
  display :flex
  position:absolute
  left:0
  right:0
  bottom:0
  line-height:.6rem
  color:#fff
  background-image:linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,.8))
  .banner-title
   flex:1
   font-size:.32rem
   padding:0 .2rem
  .banner-number   
    height:.32rem
    margin-top:.14rem
    padding:0 .4rem
    line-height :.32rem
    font-size :.24rem
    border-radius:.2rem
    background:rgba(0,0,0,.8)
     .banner-icon
      font-size:.24rem
</style>
