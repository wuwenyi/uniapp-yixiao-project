<template>
	<view class="content">
		<textarea class="in-content" placeholder="请输入文字......"></textarea>
		<image class="write-btn show-img" src="../../static/write-btn.png"></image>
		<view class="img-list">
			<view class="list">
				<image class="show-img" src="../../static/write-btn.png"></image>
				<view class="close">x</view>
			</view>
			
		</view>
		
		<view class="control">
			<view class="btn tag">添加标签</view>
			<view class="btn visit">所有人可见</view>
			<view class="btn add">发布</view>
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
	.content{
		width: 702upx;
		margin: 0 auto;
	}
	.in-content{
		margin-top: 56upx;
		line-height: 50upx;
		font-size: 30upx;
		height: 150upx;
	}
	.write-btn{
		
	}
	.show-img{
		width: 161upx;
		height: 161upx;
		margin-right: 16upx;
		margin-top: 10upx;
	}
	.list{
		width: 161upx;
		height: 161upx;
		float: left;
		position: relative;
	}
	.close{
		width: 36upx;
		height: 36upx;
		line-height: 30upx;
		font-size: 38upx;
		border-radius: 50%;
		background-color: red;
		color: white;
		text-align: center;
		position: absolute;
		top: 0;
		right: 0;
	}
	.control{
		width: 702upx;
		height: 38upx;
		text-align: center;
		position: fixed;
		bottom: 20upx;
	}
	.btn{
		background-color: #b9b9b9;
		border-radius: 20upx;
		color: #777777;
		font-size: 24upx;
		text-align: center;
		height: 38upx;
		line-height: 38upx;
		padding: 0 42upx;
	}
	.tag{
		float: left;
	}
	.visit{
		display: inline-block;
		position: relative;
		top: -10upx;
	}
	.add{
		float: right;
	}
</style>
