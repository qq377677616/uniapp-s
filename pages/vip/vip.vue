<template>
	<view>
		<view class="vip-list">
			<view class="item flex" v-for="item in 15" :key="item">
				<view class="left"><image src="../../static/images/img_02.png" mode=""></image></view>
				<view class="right flex-cen">
					<div class="box">
						<view class="h3">初级学员<text>299.00</text>元</view>
						<view class="p">初级课程+每天可接8单任务（剩余：-934）</view>
					</div>
					<view class="btn">立即升级</view>
				</view>
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
		methods: {
			
		}
	}
</script>

<style>
	.vip-list{padding:0 10rpx;padding-top: 16rpx;background: #f8f8f8;}
	.item{margin-bottom: 20rpx;border-radius: 10rpx;background: #fff;border-radius: 10rpx;overflow: hidden;}
  .item .left{width:140rpx;height:230rpx;}
	.item .left image{width: 100%;height: 100%;}
	.item .right{height: 230rpx;position: relative;padding:0 40rpx;flex: 1;}
	.item .right .box{margin-top: -20rpx;}
	.item .h3{font-size: 28rpx;margin-bottom: 10rpx;color:#4AA568;}
	.item .h3 text{font-size: 40rpx;}
	.item .p{font-size: 24rpx;}
	.item .btn{font-size: 26rpx;width: 156rpx;height: 40rpx;line-height: 40rpx;text-align: center;color:#fff;background: #4AA568;border-radius: 10rpx;position: absolute;right:40rpx;bottom:26rpx;}
</style>
