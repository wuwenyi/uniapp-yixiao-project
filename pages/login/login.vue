<template>
	<view class="content">
		<view class="title">明德一校</view>
		<view class="in-line">
			<input type="text" placeholder="邮箱" />
		</view>
		<view>
			<input type="text" placeholder="密码" />
		</view>
		<view class="register-link">
			还没有注册，<navigator url="/pages/register/register" class="link-text">注册</navigator>
		</view>
		<view>
			<button class="btn">登&nbsp;&nbsp;&nbsp;&nbsp;录</button>
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
	@import url("../../static/login.css");
</style>
