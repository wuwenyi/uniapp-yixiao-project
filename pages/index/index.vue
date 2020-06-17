<template>
	<view class="content">
		
		
		<veiw class="list" v-for="list in dataList">
			<view class="user-body">
				<view class="user-box"><image class="user-img" :src="list.userImg"></image></view>
				<view class="user-info">
					<view>{{list.userName}}</view>
					<text class="time">{{list.created_at}}</text>
				</view>
				<image class="close" src="../../static/close.png"></image>
			</view>
			<view class="title">{{list.post_title}}</view>
			<view class="img-list" v-if="list.photos">
				<image class="img-show" :src="list.photos"></image>
			</view>
			
			<view class="control">
				<view class="contrl-list">
					<image class="control-img" src="../../static/share.png"></image>
					<text class="control-num">{{list.share_count}}</text>
				</view>
				<view class="contrl-list">
					<image class="control-img" src="../../static/message.png"></image>
					<text class="control-num">{{list.focus_count}}</text>
				</view>
				<view class="contrl-list">
					<image class="control-img" src="../../static/zhan-h.png"></image>
					<text class="control-num">{{list.click_count}}</text>
				</view>
			</view>
			
		</veiw>
		
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				dataList:[]
			}
		},
		onLoad() {
			var thisObj = this;
			uni.request({
				url:'https://api.yqxbxb.com/public/api/article/third/top10',
				data:{},
				method:'get',
				success:function(res){
					console.log(res.data.data.list);
					thisObj.dataList = res.data.data.list;
				},
				fail:function(){
					
				}
			})
		
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
