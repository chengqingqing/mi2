<template>
<div class="top-sub">
  <div class="sub-1">
    <ul class="channels">
      <li class="channel" v-for="item in channels">
        <a :href="item.channelUrl" target="_blank">
          <i class="fa fa-fw sub-icon" :class="item.faclass"></i>
          <p class="channel-txt">
              {{item.name}}
          </p>
        </a>
      </li>
    </ul>
  </div>
  <ul class="subs">
    <li v-for="item in subImages">
      <a :href="item.subHref" class="sub-item sub-2" target="_blank">
        <img :src="item.subSrc" alt="" />
      </a>
    </li>
  </ul>
</div>
</template>

<script>
 export default {
  data () {
    return {
      channels: [
        {name: '选购手机', faclass: 'fa-mobile', channelUrl: 'http://www.mi.com/compare/'},
        {name: '企业团购', faclass: 'fa-gift', channelUrl: 'http://qiye.mi.com/'},
        {name: '官翻产品', faclass: 'fa-refresh', channelUrl: 'http://item.mi.com/re'},
        {name: '小米移动', faclass: 'fa-credit-card', channelUrl: 'http://huanxin.mi.com/product/list'},
        {name: '以旧换新', faclass: 'fa-recycle', channelUrl: 'http://huanxin.mi.com/product/list'},
        {name: '话费充值', faclass: 'fa-credit-card-alt', channelUrl: 'http://recharge.10046.mi.com/'}
      ],
      subImages: [
        {subHref: 'http://hd.mi.com/y/08191p/index.html', subSrc: 'http://i3.mifile.cn/a4/1327d707-4f67-4c36-8ae5-3d7704c989eb'},
        {subHref: 'http://item.mi.com/buyphone/redmipro/', subSrc: 'http://i3.mifile.cn/a4/c202123c-4197-4666-9793-2f1e156ab23a'},
        {subHref: 'http://item.mi.com/static/buymipad', subSrc: 'http://i3.mifile.cn/a4/216f7f38-66ee-4c1b-8409-8d77cb64d386'}
      ]

    }
  }
 }

</script>

<style scoped>
.top-sub {
	position: relative;
	width: 1226px;
	height: auto;
	margin: 14px auto 26px;
}
.sub-1 {
	float: left;
	width: 234px;
	height: 170px;
	background: #5f5750;
}
.channels{
	display: flex;
	flex-flow: row wrap;
	justify-content: flex-start;
	align-items: flex-start;
	list-style: none;
	margin: 0;
	padding: 3px;
	.channel a {
		width: 75px;
    text-decoration: none;
		height: 82px;
		cursor: pointer;

		&:hover{
			.channel-txt {
				color: #fff;
			}
			.sub-icon {
				color: #fff;
			}
		}
		.channel-txt {
			display: block;
      margin: 0;
			width: 75px;
      padding-bottom:18px;
			font-size: 12px;
			text-align: center;
			text-decoration: none;
			color: rgba(255,255,255,0.7);
		}
	}
	.sub-icon {
		width: 75px;
		height: 24px;
		margin-top: 18px;
		margin-bottom: 5px;
		font-size: 20px;
		color: rgba(255,255,255,0.7);
	}
}

.subs {
	display: flex;
	flex-flow: row nowrap;
	justify-content: flex-start;
	margin: 0;
	padding: 0;
	list-style: none;
	li {
		width: 316px;
		height: 170px;
		margin-left: 15px;
	}
	.sub-item {
		display: block;
		transition: all 0.3s;
		&:hover {
			box-shadow: 0 5px 30px #ccc;
		}
		img {
			display: block;
			width: 316px;
			height: 170px;
		}
	}
}

.line-vertical {
	width: 1px;
	height: 60px;
	margin-top: 10px;
	background: rgba(255,255,255,0.1);
}

.line-horizontal {
	width: 60px;
	height: 1px;
	margin: 0 8px;
	background: rgba(255,255,255,0.1);
}

</style>
