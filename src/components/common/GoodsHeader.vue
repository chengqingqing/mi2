<template>
  <div class="header-wrap">
		<h2 class="title">{{title}}</h2>
	</div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    }
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
.header-wrap 
	position: relative
	.title
		margin: 0;
		font-size: 22px;
		font-weight: 200;
		line-height: 58px;
		color: #333;
</style>
