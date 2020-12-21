<template>
	<view class="content">
		<view class="logo">
			<image class="logo" src="../../static/img/logo.png" mode=""></image>
		</view>
		<view class="main">
			<view class="uni-form-item uni-column" >
				<view class="title">账号</view>
				<input class="input" focus placeholder="请输入账号" />
			</view>
			<view class="uni-form-item uni-column">
				<view class="title">密码</view>
				<input class="input" password type="text" placeholder="请输入密码" />
			</view>
			<checkbox-group style="margin-top: 20rpx;">
				<label>
					<checkbox value="cb"  color="#2F6DE0" style="transform:scale(0.7);float: left;color:rgba(47,109,224,1);" />
					<view class="txt" style="font-size: 28rpx;float: left;margin-top: 10rpx;color:#2F6DE0;font-weight: 500;">
						保存密码
					</view>
				</label>
			</checkbox-group>
			<view class="button">
				<button  class="enter" @tap="enter">登录</button>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		onLoad() {
	
		},
		methods: {
			enter(){
				uni.reLaunch({
					url: '../WorkBench/WorkBenchIndex',
				});
			}
		}
	}
</script>

<style lang="scss">
	@import url("../../static/iconfont/iconfont.css");
	.content{
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		.logo{
			width: 120rpx;
			height: 120rpx;
			margin-top: 80rpx;
		}
		.main{
			margin-top: 150rpx;
			width: 690rpx;
			height: 550rpx;

			.title{
				font-size:28rpx;
				font-family:PingFang SC;
				font-weight:500;
				color:rgba(51,51,51,1);
				margin: 40rpx 0;
			}
			.input{
				height: 80rpx;
				border-bottom: 2rpx solid rgba(213,217,225,1);
				background-color: #FFF !important;
				.uni-input-input{
					background-color: #FFF !important;
				}
			}
			.button{
				margin-top: 120rpx;
				.enter{
					width: 690rpx;
					background:rgba(47,109,224,1);
					color: #fff;
					font-size: 36rpx;
				}
			}
			
			
		}
		
		
	}
</style>
