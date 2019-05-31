<template>
<div>
  <div class="banner" @click='handleBannerClick'>
     <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1902/84/84696f368bbec10da3.img.jpg_600x330_5ca3e181.jpg" />
     <div class="banner-info">
       <div class="banner-title">北京世界园艺博览会</div>
       <div class="banner-number"><span class="iconfont banner-icon">&#xe623;</span>9</div>
     </div>
  </div>
   <common-gallery :imgs='imgs' v-show='showGallery' @close='handleGalleryClose'></common-gallery>
</div> 
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'
export default {
   name:'DetailBanner',
   data(){
     return{
       imgs:['http://img1.qunarzz.com/sight/p0/1902/84/84696f368bbec10da3.img.jpg_350x240_3a0fefe8.jpg',
      'http://img1.qunarzz.com/sight/p0/1902/3b/3bc5185f2bc00e49a3.img.jpg_350x240_3042e6e0.jpg'],
      showGallery:false
     }
   },
   methods:{
    handleBannerClick(){
      this.showGallery=true
    },
    handleGalleryClose(){
      this.showGallery=false
    }
   },
   components:{
     CommonGallery
   }
}
</script>

<style lang='stylus' scoped>
.banner 
 position relative
 overflow hidden
 height 0
 padding-bottom 55%
.banner-img
 width 100%
.banner-info
 display flex
 position absolute
 left 0
 right 0
 bottom 0
 line-height .6rem
 color #fff
 background-image linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,.8))
.banner-title 
 flex 1
 font-size .32rem
 padding 0 .2rem
.banner-number
 height .32rem
 line-height .32rem
 margin-top .14rem
 padding 0 .4rem
 border-radius .2rem
 background rgba(0,0,0,.8)
 font-size .24rem
.banner-icon
 font-size .24rem
 margin-right .02rem
</style>
