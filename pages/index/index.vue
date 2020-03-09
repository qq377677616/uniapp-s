<template>
	<view class="body">
		<!-- 标题部分 -->
	  <view class="title flex" @click="jump">
			<view class="flex-cen item">
				<image src="../../static/images/img_01.png" mode="widthFix"></image>
				<text class="span">抖音</text>
			</view>
		</view>
		<!-- 任务列表部分 -->
		<view class="task-list">
			<view v-for="item in 15" :key="item" class="item flex">
				<view class="left flex">
					<view class="flex">
						<view class="img"><image src="../../static/images/img_01.png" mode="widthFix"></image></view>
						<view class="text">
							<view class="p">任务描述：点赞|关注</view>
							<view class="p">需求方：抖音2</view>
							<text class="surplus">剩余14526</text>
						</view>
					</view>
				</view>
				<view class="right flex-cen">
					<view class="num">2元</view>
					<view class="btn">接任务</view>
				</view>
			</view>
		</view>
		<!-- #ifdef APP-PLUS -->
		<button class="bottom" type="primary" @click="appWxMaLogin" withCredentials="true">跳转小程序登陆</button>
		<!-- #endif -->
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {
			uni.showToast({ title: "hello world" })
			console.log("这是条件编译")
		},
		methods: {
			//跳转app
      jump() {
				plus.runtime.openURL("https://v.douyin.com/nkeNuB/", res => {
					console.log("跳转成功")
				})
			},
			//跳转微信小程序
			appWxMaLogin: function() {
				// 调用微信小程序
				console.log('调用微信小程序');
				// #ifdef APP-PLUS
				plus.share.getServices(
					function(res) {
						var sweixin = null;
						for (var i = 0; i < res.length; i++) {
							var t = res[i];
							if (t.id == 'weixin') {
								sweixin = t;
							}
						}
						if (sweixin) {
							sweixin.launchMiniProgram({
								id: 'wx9cb717d8151d8486', // 要跳转小程序的原始ID
								path: 'pages/index/index',
								type: 2 // 微信小程序版本类型可取值： 0-正式版； 1-测试版； 2-体验版。 默认值为0。
							});
						}
					},
					function(res) {
						console.log(JSON.stringify(res));
					}
				);
				// #endif
			}
		}
	}
</script>

<style>
	.task-list{background: #F8F8F8;}
	/* .scroll-Y{height:100%;} */
	.title{height: 86rpx;}
	.title image{width:44rpx;height:44rpx;}
	.title .span{font-size: 28rpx;padding-left: 8rpx;}
  .title .item{padding:0 42rpx;position: relative;}
	.title .item::after{content:"";display: block;width:100%;height:4rpx;background: #4AA568;position: absolute;left:0;bottom:0;}
	.task-list{padding:20rpx 10rpx;}
	.task-list image{width:50rpx;height: 50rpx;}
	.task-list .item{justify-content: space-between ;background: #eee;border-radius: 10rpx;margin-bottom: 15rpx;}
	.task-list .text{font-size: 28rpx;line-height: 44rpx;padding-left: 20rpx;}
	.task-list .left{flex-direction: column;padding-left: 25rpx;padding:28rpx 0 28rpx 26rpx;}
	.task-list .right{background: #fff;flex-direction: column;color:#4AA568;padding:0 20rpx;}
	.task-list .right .num{font-size: 30rpx;font-weight: bold;padding-bottom: 10rpx;}
	.task-list .right .btn{width:138rpx;line-height: 40rpx;font-size: 26rpx;color:#fff;background: #4AA568;border-radius: 40rpx;text-align: center;}
	.task-list .surplus{padding:0 16rpx;height: 34rpx;line-height: 34rpx;border-radius: 34rpx;border:1px solid #4AA568;color:#4AA568;font-size: 26rpx;}
</style>
