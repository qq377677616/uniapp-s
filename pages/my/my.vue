<template>
	<view class="body">
		<!-- 个人信息部分 -->
		<view class="user">
			<view class="flex-bet">
				<view class="flex-cen">
					<view class="avatar"><image src="../../static/images/img_03.png" mode="widthFix"></image></view>
					<view>
						<view class="h3">345D5</view>
						<view class="p">15574859685</view>
					</view>
				</view>
				<view class="icon"><text class="iconfont icon-shezhi"></text></view>
			</view>
		</view>
		<!-- 总收益部分 -->
		<view class="money">
			<view class="flex-bet">
				<view class="left">
					<view class="p">总收益</view>
					<view class="money-num">0.00</view>
				</view>
				<view class="top flex-col">
					<view class="h4 flex">
						<view class="text">无法领取任务</view>
						<view class="flex-cen"><image src="../../static/images/vip_01.png" mode="widthFix" v-if="vip_grade == 0"></image><image src="../../static/images/vip_02.png" mode="widthFix" v-if="vip_grade == 1"></image><image src="../../static/images/vip_03.png" mode="widthFix" v-if="vip_grade == 2"></image>普通会员</view>
					</view>
					<view class="h5">推荐人：谷艳丽</view>
				</view>
			</view>
		</view>
		<!-- 资讯轮播部分 -->
		<view class="news">
			<view class="flex-cen">
				<view class="icon"><text class="iconfont icon-lingdang"></text></view>
				<view class="flex1">
					<swiper class="swiper" vertical="true" autoplay="true" interval="2000" >
						<swiper-item v-for="item in 20"><view class="news-item">恭喜{{item}}8AB9升级为高级学员</view></swiper-item>
				  </swiper>
				</view>
			</view>
		</view>
		<!-- 宣传图部分 -->
		<view class="banner">
			<image src="../../static/images/img_04.png" mode="widthFix"></image>
		</view>
		<!-- 功能列表部分 -->
		<view class="icons">
			<view class="icon-list">
				<view class="item">
					<text class="iconfont icon-laba"></text>
					<view class="p">我的团队</view>
				</view>
				<view class="item">
					<text class="iconfont icon-zongshouyi"></text>
					<view class="p">总收益</view>
				</view>
				<view class="item">
					<text class="iconfont icon-fenxiang"></text>
					<view class="p">分享链接</view>
				</view>
				<view class="item">
					<text class="iconfont icon-zhifubao"></text>
					<view class="p">支付宝绑定</view>
				</view>
				<view class="item">
					<text class="iconfont icon-gonggao"></text>
					<view class="p">平台公告</view>
				</view>
				<view class="item">
					<text class="iconfont icon-kefu"></text>
					<view class="p">在线客服</view>
				</view>
				<view class="item">
					<text class="iconfont icon-hezuo"></text>
					<view class="p">商家合作</view>
				</view>
				<view class="item">
					<text class="iconfont icon-icon"></text>
					<view class="p">个人中心</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				vip_grade: 0
			}
		},
		methods: {
			
		}
	}
</script>

<style>
  text{font-size: 50px;color:green;}
	.body{min-height:100%;}
	.user{padding:16px 20px;background: #fff;}
	.user image{width:102rpx;height:102rpx;border-radius: 50%;margin-right: 15rpx;}
	.user .h3,.user .p{font-size: 26rpx;color:#333;font-weight: bold;}
	.user .p{color:#666;}
	.user text{font-size: 50rpx;color:#4d4d4d;}
	.money{padding:30rpx 0 40rpx;}
	.money .left{padding-left: 35rpx;}
	.money .p{font-size: 30rpx;margin-bottom: 10rpx;}
	.money .money-num{font-size: 40rpx;color:#4AA568;}
	.money .h4{font-size: 24rpx;margin-bottom: 20rpx;padding-right: 10rpx;}
	.money .h4 .text{margin-right: 14rpx;}
	.money image{width:30rpx;margin-right: 8rpx;}
	.money .top{align-items: flex-end;}
	.money .h5{width:206rpx;line-height: 36rpx;height: 36rpx;border-radius:36rpx 0 0 36rpx;font-size: 24rpx;color:#fff;text-align: center;background: #4AA568;}
	.news{background: #eee;}
	.news .icon{padding:0 28rpx 0 30rpx;}
	.news text{font-size: 38rpx;color:#4AA568;}
	.news swiper,.news .news-item{height: 62rpx;line-height: 62rpx;font-size: 28rpx;}
	.banner{padding:10rpx;}
	.banner image{width:100%;}
  .icons{margin-top: 54rpx;}
	.icons .icon-list{font-size: 0;}
	.icons .item{width:25%;display: inline-block;vertical-align: top;font-size: 26rpx;text-align: center;margin-bottom: 50rpx;}
	.icons text{font-size: 50rpx;color:#7c7c7c;}
	.icons .p{padding-top: 16rpx;}
</style>
