<template>
  <ul class="goods-left">
    <li v-for="item in leftGoods" class="goods-left-item item-top">
      <a :href="item.sourceUrl" target="_blank">
        <img :src="item.imgUrl" alt="">
      </a>
    </li>
  </ul>
</template>

<script scoped>
export default {
  props: {
    leftGoods: {
      type: Array,
      required: true
    }
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  .goods-left
    float left
    width 234px
    height auto
    .goods-left-item
		  width 234px
      height 300px
      margin-bottom 14px
      cursor pointer
      transition all 0.3s
    & hover
      transform: translateY(-2px)
      box-shadow 5px 5px 20px #ccc
    img
      width 234px
      height 300px
    .item-bottom
      margin-top 14px
</style>
