<template>
	<view class="content">
		<view class="top">
			<view class="company">济南城投建设发展有限公司</view>
			<view class="slogan">胜人者有力，自胜者强</view>
		</view>
		<view class="main">
			<ul class="plate">
				<li class="box" @tap="attendanceclock">
					<view class="iconfont icon-wangluobanji" style="background: rgba(60,127,252,1);"></view>
					<span class="txt">考勤打卡</span>
				</li>
				<li class="box" @tap="examine">
					<view class="iconfont icon-shenpiliuchengguanli" style="background: rgba(60,127,252,1);"></view>
					<span class="txt">移动审批</span>
				</li>
				<li class="box" @tap="announcement">
					<view class="iconfont icon-tongzhi" style="background: rgba(240,66,82,1);"></view>
					<span class="txt">通知公告</span>
				</li>
				<li class="box" @tap="statement">
					<view class="iconfont icon-baobiao" style="background: rgba(46,192,111,1);"></view>
					<span class="txt">移动报表</span>
				</li>
				<li class="box" @tap="conference">
					<view class="iconfont icon-blackboard" style="background: rgba(46,192,111,1);"></view>
					<span class="txt">会议管理</span>
				</li>
				<li class="box" @tap="pushmoney">
					<view class="iconfont icon-leijishouyi" style="background: rgba(240,123,66,1);"></view>
					<span class="txt">提成管理</span>
				</li>
			</ul>
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
			//考勤打卡
			attendanceclock(){
				console.log('考勤打卡');
			},
			//移动审批
			examine(){
				console.log('移动审批');
			},
			//通知公告
			announcement(){
				console.log('通知公告');
			},
			//移动报表
			statement(){
				console.log('移动报表');
			},
			//会议管理
			conference(){
				console.log('会议管理');
			},
			//提成管理
			pushmoney(){
				console.log('提成管理');
			},
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
		.top{
			width:750rpx;
			height:400rpx;
			background:linear-gradient(0deg,rgba(49,200,232,1)0%,rgba(47,109,224,1) 99%);
			display: flex;
			flex-direction: column;
			align-items: center;
			.company{
				height:34rpx;
				font-size:36rpx;
				font-family:PingFang SC;
				// font-weight:bold;
				color:rgba(255,255,255,1);
				margin-top: 65rpx;
			}
			.slogan{
				height:49rpx;
				font-size:48rpx;
				font-family:PingFang SC;
				// font-weight:bold;
				color:rgba(255,255,255,1);
				margin-top: 130rpx;
			}
		}
		.main{
			.plate{
				margin-top: 100rpx;
				list-style: none;
				margin-left: 30rpx;
				.box{
					width: 33%;
					height: 250rpx;
					float: left;
					.iconfont{
						display: flex;
						flex-direction: column;
						align-items: center;
						justify-content: center;
						width: 100rpx;
						height: 100rpx;
						font-size: 60rpx;
						color: #fff;
						border-radius:38%;
					}
					.txt{
						width:109rpx;
						height:26rpx;
						font-size:28rpx;
						font-family:PingFang SC;
						font-weight:400;
						color:rgba(51,51,51,1);
						margin-left: -6rpx;
					}
				}
				
			}
		}
	}
	
</style>
