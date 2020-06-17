<template>
	<view class="content">
		
		
		<veiw class="list">
			<view class="user-body">
				<view class="user-box"><image class="user-img" src="../../static/show/user-img.png"></image></view>
				<view class="user-info">
					<view>今生友缘</view>
					<text class="time">1分钟前</text>
				</view>
				<image class="close" src="../../static/close.png"></image>
			</view>
			<view class="title">马上毕业了，有床帘闲置，有哪位小可爱要入吗，价格88元，含支架</view>
			<view class="img-list">
				<image class="img-show" src="../../static/show/show1.jpg"></image>
				<image class="img-show" src="../../static/show/show1.jpg"></image>
				<image class="img-show" src="../../static/show/show1.jpg"></image>
				<image class="img-show" src="../../static/show/show1.jpg"></image>
				<image class="img-show" src="../../static/show/show1.jpg"></image>
			</view>
			
			<view class="control">
				<view class="contrl-list">
					<image class="control-img" src="../../static/share.png"></image>
					<text class="control-num">25</text>
				</view>
				<view class="contrl-list">
					<image class="control-img" src="../../static/message.png"></image>
					<text class="control-num">253</text>
				</view>
				<view class="contrl-list">
					<image class="control-img" src="../../static/zhan-h.png"></image>
					<text class="control-num">235</text>
				</view>
			</view>
			
		</veiw>
		
		<veiw class="list">
			<view class="user-body">
				<view class="user-box"><image class="user-img" src="../../static/show/user-img.png"></image></view>
				<view class="user-info">
					<view>今生友缘</view>
					<text class="time">1分钟前</text>
				</view>
				<image class="close" src="../../static/close.png"></image>
			</view>
			<view class="title">马上毕业了，有床帘闲置，有哪位小可爱要入吗，价格88元，含支架</view>
			<view class="img-list">
				<image class="img-show" src="../../static/show/show1.jpg"></image>
				<image class="img-show" src="../../static/show/show1.jpg"></image>
				<image class="img-show" src="../../static/show/show1.jpg"></image>
				<image class="img-show" src="../../static/show/show1.jpg"></image>
				<image class="img-show" src="../../static/show/show1.jpg"></image>
			</view>
			
			<view class="control">
				<view class="contrl-list">
					<image class="control-img" src="../../static/share.png"></image>
					<text class="control-num">25</text>
				</view>
				<view class="contrl-list">
					<image class="control-img" src="../../static/message.png"></image>
					<text class="control-num">253</text>
				</view>
				<view class="contrl-list">
					<image class="control-img" src="../../static/zhan-h.png"></image>
					<text class="control-num">235</text>
				</view>
			</view>
			
		</veiw>
		
		
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

		},
		methods: {

		}
	}
</script>

<style>
	body{
		padding-top: 16upx;
	}
	.content {
	
	}
	.list{
		border-bottom: 15upx solid #e5e5e5;
		clear: both;
		display: block;
	}
	.user-box .user-img{
		width: 65upx;
		height: 65upx;
		border-radius: 50%;
		overflow: hidden;
	}
	.user-box{
		margin-left: 25upx;
		float: left;
	}
	.user-info{
		float: left;
		font-size: 28upx;
		margin-left: 16upx;
	}
	.time{
		font-size: 23upx;
		color: #a2a2a2;
	}
	.close{
		width: 16upx;
		height: 16upx;
		float: right;
		margin-right: 23upx;
		margin-top: 12upx;
	}
	.user-body{
		clear: both;
		height: 68upx;
	}
	
	.title{
		width: 673upx;
		font-size: 30upx;
		color: #353535;
		margin-left: 42upx;
		clear: both;
		line-height: 40upx;
	}
	.img-list{
		width: 687upx;
		margin:0 auto;
	}
	.img-show{
		width: 30%;
		height: 200upx;
		margin: 10upx 1.5%;
	}
	.control{
		height: 60upx;
	}
	.contrl-list{
		float: left;
		width: 33%;
		text-align: center;
	}
	.control-img{	
		width: 35upx;
		height: 29upx;
	}
	.control-num{
		font-size: 21upx;
		color: #7f7e7e;
		position: relative;
		top: -4upx;
		margin-left: 14upx;
	}
</style>
