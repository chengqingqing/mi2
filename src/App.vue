<template>
  <div id="app">
    <topbar></topbar>
    <topheader></topheader>
    <topbanner></topbanner>
    <top-sub></top-sub>
    <div class="goods-container">
      <goods-top-box></goods-top-box>
      <goods-collocation></goods-collocation>
		  <goods-accessories></goods-accessories>
		  <goods-around></goods-around>
		  <recommend></recommend>
		  <hot-product></hot-product>
		  <goods-content></goods-content>
		  <video></video>
      <temp-footer></temp-footer>
      <play-video :play-config="playConfig"></play-video>

    </div>

  </div>
</template>

<script>
  import topbar from './components/TopBar'
  import topheader from './components/TopHeader'
  import topbanner from './components/TopBanner'
  import TopSub from './components/TopSub'

  import GoodsTopBox from './components/GoodsTopBox'
  import GoodsCollocation from './components/GoodsCollocation'
  import GoodsAccessories from './components/GoodsAccessories'
  import GoodsAround from './components/GoodsAround'
  import Recommend from './components/Recommend'
  import HotProduct from './components/HotProduct'
  import GoodsContent from './components/GoodsContent'
  import TempFooter from './components/TempFooter'
  import Video from './components/Video'
  import PlayVideo from './components/PlayVideo'

  export default {
    data () {
      return {
        playConfig: {}
      }
    },
    ready () {
      this.recivePlayVideo()
    },
    methods: {
      recivePlayVideo () {
        this.$on('play', function (opts) {
          this.playConfig = opts
        })
      }
    },
    components: {
      topbar,
      topheader,
      topbanner,
      'top-sub': TopSub,
      'goods-top-box': GoodsTopBox,
      'goods-collocation': GoodsCollocation,
      'goods-accessories': GoodsAccessories,
      'goods-around': GoodsAround,
      'recommend': Recommend,
      'hot-product': HotProduct,
      'goods-content': GoodsContent,
      TempFooter,
      'video': Video,
      'play-video': PlayVideo
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
@import './assets/css/base.css'
.goods-container
	width: 100%
	height: auto
	background: #f5f5f5
	padding-bottom: 40px

</style>
