<template>
	<view>
		<view class="list">
			<image class="list-icon" src="../../static/at.png"></image>
			<text class="title">@我的</text>
			<image class="right-in" src="../../static/right-in.png"></image>
		</view>
		<view class="list">
			<image class="list-icon" src="../../static/chat.png"></image>
			<text class="title">评论</text>
			<image class="right-in" src="../../static/right-in.png"></image>
		</view>
		<view class="list">
			<image class="list-icon" src="../../static/dianzan.png"></image>
			<text class="title">点赞</text>
			<image class="right-in" src="../../static/right-in.png"></image>
		</view>
		<view class="list">
			<image class="list-icon" src="../../static/tongzhi.png"></image>
			<text class="title">通知信息</text>
			<image class="right-in" src="../../static/right-in.png"></image>
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
	.list{
		height: 130upx;
		/* margin-left: 30upx; */
		padding-left: 30upx;
		padding-right: 42upx;
		clear: both;
		border-bottom:1upx solid #e7e7e7;
	}
	.list-icon{
		width: 97upx;
		height: 97upx;
		margin-top: 13upx;
		float: left;
	}
	.title{
		font-size: 32upx;
		color: #333333;
		line-height: 130upx;
		float: left;
		margin-left: 23upx;
	}
	.right-in{
		width: 14upx;
		height: 24upx;
		float: right;
		margin-top:54upx;
	}
</style>
