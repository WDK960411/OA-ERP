<template>
	<view class="content">
		<view class="headtitle">通讯录</view>
		<view class="main">
			
		</view>
		<Index></Index>
	</view>
</template>

<script>
	import Index from "../index/index.vue"
	export default {
		components:{
			Index,
		},
		data() {
			return {
				
			}
		},
		onLoad() {
	
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	@import url("../../static/iconfont/iconfont.css");
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		.headtitle{
			width:150rpx;
			height:46rpx;
			font-size:48rpx;
			font-family:PingFang SC;
			font-weight:bold;
			color:rgba(51,51,51,1);
			position: relative;
			top: 60rpx;
			left: -260rpx;
		}
		.main{
			width: 660rpx;
			margin-top: 100rpx;
			
		}
		
	}
</style>
