<template>
	<view class="content">
		<view class="top">
			<view class="iconfont icon-fanhui" style="color: rgba(51,51,51,1);" @tap="getback"></view>
			<view class="txt">消息详情</view>
		</view>
		<view class="main">
			<view class="infoparticulars" v-for="(item,index) in datas">
				<view class="dateline">
					<view class="date">{{item.date}}</view>
					<view class="time">{{item.time}}</view>
				</view>
				<view class="infotxt">{{item.info}}</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				datas:[
					{
						index: 0,
						status: "read",
						info:"办公自动化没有统一的定义，凡是在传统的办公室中采用各种新技术、新机器、新设备从事办公业务，都属于办公自动化的领域。",
						date:"03/02",
						time:"11:30"
					}
				]
			}
		},
		onLoad() {
	
		},
		methods: {
			//返回
			getback(){
				uni.navigateTo({
				    url: '../Information'
				});
			},	
			//拨打电话
			call(){
				uni.makePhoneCall({
				    phoneNumber: '400-800-5888' 
				});
			}
		}
	}
</script>

<style lang="scss">
	@import url("../../../static/iconfont/iconfont.css");
	.content{
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		.top{
			width: 100%;
			height: 90rpx;
			border-bottom: 2rpx solid #eee;
			.iconfont{
				font-size: 40rpx;
				color: rgba(51,51,51,1);
				float: left;
				margin-top: 20rpx;
			}
			.txt{
				font-size:36rpx;
				font-family:PingFang SC;
				font-weight:bold;
				color:rgba(51,51,51,1);
				text-align: center;
				margin-top: 20rpx;
			}
		}
		.main{
			width: 670rpx;
			margin-top: 50rpx;
			.infoparticulars{
				.dateline{
					width: 100%;
					display: flex;
					align-items: center;
					justify-content: center;
					.date, .time{
						width:60rpx;
						font-size:24rpx;
						font-family:PingFang SC;
						font-weight:400;
						color:rgba(102,102,102,1);
						float: left;
						margin-left: 15rpx;
					}
				}
				.infotxt{
					font-size:28rpx;
					line-height: 50rpx;
					font-family:PingFang SC;
					font-weight:500;
					color:rgba(51,51,51,1);
					float: left;
					margin-top: 28rpx;
				}
			}
		}
	}
</style>
