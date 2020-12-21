<template>
	<view class="content">
		<view class="footer">
			<ul>
				<li class="navbar" @tap="info">
					<view class="info">
						<view class="iconfont icon-xiaoxi"></view>
						<span class="txt">消息</span>
					</view>
				</li>
				<li class="navbar" @tap="workbench">
					<view class="workbench">
						<view class="iconfont icon-gaiicon-"></view>
						<span class="txt">工作台</span>
					</view>
				</li>
				<li class="navbar" @tap="addresslist">
					<view class="addresslist">
						<view class="iconfont icon-tongxunlu"></view>
						<span class="txt">通讯录</span>
					</view>
				</li>
				<li class="navbar" @tap="my">
					<view class="my">
						<view class="iconfont icon-wode"></view>
						<span class="txt">我的</span>
					</view>
				</li>
			</ul>
		</view>
	</view>
</template>

<script>
	// import Information from "Information/Information.vue"
	// import WorkBench from "WorkBench/WorkBenchIndex.vue"
	// import AddressList from "AddressList/AddressList.vue"
	// import My from "My/My.vue"
	export default {
		components:{
			// Information,
			// WorkBenchIndex,
			// AddressList,
			// My
		},
		data() {
			return {
				
			}
		},
		onLoad() {

		},
		methods: {
			info(){
				uni.navigateTo({
				    url: '../Information/Information'
				});
			},
			workbench(){
				uni.reLaunch({
				    url: '../WorkBench/WorkBenchIndex'
				});
			},
			addresslist(){
				uni.navigateTo({
				    url: '../AddressList/AddressList'
				});
			},
			my(){
				uni.navigateTo({
				    url: '../My/My'
				});
			}
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
		.footer{
			width: 100%;
			height: 100rpx;
			position: fixed;
			bottom: 0;
			z-index: 999;
			background: #fff;
			margin: 0;
			padding: 0;
			border-top: 3rpx solid #eee;
			.navbar{
				list-style: none;
				float: left;
				font-size: 24rpx;
				width: 25%;
				color:rgba(153,153,153,1);
				margin-top: 5rpx;
				text-align: center;
				margin-left: -40rpx;
				margin-right: 40rpx;
				.iconfont{
					font-size: 40rpx;
					margin-bottom: 5rpx;
				}
				.txt{
					width:69rpx;
					height:23rpx;
					text-align: center;
				}
			}
		}
	}
</style>
