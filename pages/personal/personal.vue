<template>
	<view class="">
		<view class="top-hang content">
			<view class="user-img" >
				<image src="../../static/show/user-img.png"></image>
			</view>
			<view class="user-info">
				<view class="user-name">
					<image class="vip-icon" src="../../static/vip.png"></image>
					大大大奇葩
					<image class="sex-icon" src="../../static/woman.png"></image>
				</view>
				<view class="editor">查看个人主页、编辑资料</view>
			</view>
		</view>
		<view class="nav content">
			<view class="nav-line">
				<text class="num">10</text>
				<view class="care">关注</view>
			</view>
			<view class="nav-line nav-two">
				<text class="num">10500</text>
				<view class="care">粉丝</view>
			</view>
			<view class="nav-line nav-three">
				<text class="num">1000</text>
				<view class="care">我的发文</view>
			</view>
			
			<view class="nav-last">
				<image class="add-icon" src="../../static/write-icon.png"></image>
				<text class="qiandao">签到</text>
			</view>
		</view>
		<view class="hr"></view>
		
		<view>
			<view class="list">
				<image class="list-icon" src="../../static/star.png"></image>
				收藏
			</view>
			<view class="list">
				<image class="list-icon" src="../../static/history.png"></image>
				浏览历史
			</view>
			<view class="list">
				<image class="list-icon" src="../../static/database.png"></image>
				我的积分
			</view>
			<view class="list">
				<image class="list-icon" src="../../static/setting.png"></image>
				设置
			</view>
			<view class="list">
				<image class="list-icon" src="../../static/notic.png"></image>
				关于
			</view>
		</view>
		
		
		
		<navigator url="/pages/login/login">跳转到登录页面</navigator>
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
	.content{
		width: 694upx;
		margin: 0 auto;
	}
	.user-img,.user-img image{
		width: 128upx;
		height: 128upx;
		border-radius: 50%;
		overflow: hidden;
		float: left;
	}
	.top-hang{
		height: 128upx;
	}
	.user-img{
		margin-top: 20upx;
	}
	.vip-icon{
		width: 26upx;
		height: 23upx;
		margin-right: 10upx;
	}
	.sex-icon{
		width: 26upx;
		height: 26upx;
		margin-left:20upx ;
	}
	.editor{
		padding-left: 10upx;
	}
	.user-info{
		float: left;
		margin-left: 55upx;
		font-size: 24upx;
		font-family: 黑体;
		margin-top: 40upx;
	}
	.user-name{
		font-size: 38upx;
		margin-bottom: 22upx;
	}
	.nav{
		clear: both;
		height: 70upx;
		margin-top: 66upx;
	}
	.nav-line{
		width: 124upx;
		text-align: center;
		float: left;
	}
	.num{
		font-size: 36upx;
	}
	.care{
		font-size: 24upx;
	}
	.nav-two{
		width: 170upx;
	}
	.nav-three{
		width: 158upx;
	}
	.add-icon{
		width: 22upx;
		height: 21upx;
		margin-right: 16upx;
	}
	.nav-last{
		float: right;
		width: 130upx;
		height: 54upx;
		line-height: 54upx;
		border-radius: 22upx;
		background-color: #00a0e9;
		text-align: center;
		margin-right: 3upx;
		font-size: 24upx;
	}
	.hr{
		height: 12upx;
		background-color: #e7e7e7;
		margin-top: 35upx;
		clear: both;
	}
	.list{
		margin: 0 auto;
		height: 67upx;
		padding: 53upx 30upx 0 30upx;
		font-size: 32upx;
		line-height: 32upx;
		border-bottom: 1upx solid #e7e7e7;
	}
	.list-icon{
		width: 35upx;
		height: 33upx;
		margin-right: 30upx;
		position: relative;
		top: 5upx;
	}
</style>
