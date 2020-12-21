<template>
	<view class="content">
		<view class="headtitle">消息</view>
		<view class="main">
			<view :class="'info'+item.status" v-for="(item,index) in datas" @tap="infoparticulars" :id="'info'+item.index">
				<image src="../../static/img/read.png" class="read" v-if="item.status=='read'">
				<image src="../../static/img/unread.png" class="unread" v-if="item.status=='unread'">
				<view class="redhint" v-if="item.status=='unread'"></view>
				<view class="infonews">{{item.info}}</view>
				<view class="date">{{item.date}}</view>
				<view class="time">{{item.time}}</view>
			</view>
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
				datas:[
					{
						index: 0,
						status: "unread",
						info:"办公自动化没有统一的定义，凡是在传统的办公室中采用各种新技术、新机器、新设备从事办公业务，都属于办公自动化的领域。",
						date:"03/02",
						time:"11:30"
					},
					{
						index: 1,
						status: "unread",
						info:"办公自动化没有统一的定义，凡是在传统的办公室中采用各种新技术、新机器、新设备从事办公业务，都属于办公自动化的领域。",
						date:"03/02",
						time:"11:30"
					},
					{
						index: 2,
						status: "read",
						info:"办公自动化没有统一的定义，凡是在传统的办公室中采用各种新技术、新机器、新设备从事办公业务，都属于办公自动化的领域。",
						date:"03/02",
						time:"11:30"
					},
					{
						index: 3,
						status: "read",
						info:"办公自动化没有统一的定义，凡是在传统的办公室中采用各种新技术、新机器、新设备从事办公业务，都属于办公自动化的领域。",
						date:"03/02",
						time:"11:30"
					},
					{
						index: 4,
						status: "read",
						info:"办公自动化没有统一的定义，凡是在传统的办公室中采用各种新技术、新机器、新设备从事办公业务，都属于办公自动化的领域。",
						date:"03/02",
						time:"11:30"
					},
					{
						index: 5,
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
			//点击进入消息详情
			infoparticulars(e){
				uni.navigateTo({
				    url: './Model/InfoParticulars'
				});
				console.log(e);
				console.log(e.currentTarget.id);
			},
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
			width:100rpx;
			height:46rpx;
			font-size:48rpx;
			font-family:PingFang SC;
			font-weight:bold;
			color:rgba(51,51,51,1);
			position: relative;
			top: 60rpx;
			left: -280rpx;
		}
		.main{
			width: 660rpx;
			margin-top: 100rpx;
			.inforead, .infounread{
				width: 670rpx;
				height: 110rpx;
				border-bottom: 1rpx solid rgba(213,217,225,1);
				line-height: 110rpx;
				.read, .unread{
					width: 48rpx;
					height: 48rpx;
					float: left;
					margin-top: 30rpx;
				}
				.unread{
					margin-top: 36rpx;
				}
				.redhint{
					width: 13rpx;
					height: 13rpx;
					border-radius: 50%;
					background-color: #FF3950;
					float: left;
					position: relative;
					top: 40rpx;
					left: -10rpx;
				}
				.infonews{
					width:460rpx;
					font-size:28rpx;
					font-family:PingFang SC;
					font-weight:500;
					color:#888;
					float: left;
					overflow:hidden; //超出一行文字自动隐藏
					text-overflow:ellipsis;//文字隐藏后添加省略号
					white-space:nowrap; //强制不换行
					margin-left: 10rpx;
				}
				.date, .time{
					width:65rpx;
					font-size:24rpx;
					font-family:PingFang SC;
					font-weight:400;
					color:rgba(102,102,102,1);
					float: left;
					margin-left: 10rpx;
				}
			}
			.infounread .infonews{
				margin-left: 0rpx;
				color: #333!important;
			}
		}
		
	}
</style>
