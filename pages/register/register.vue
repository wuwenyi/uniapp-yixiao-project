<template>
	<view class="content">
		<view class="title">明德一校</view>
		<view class="in-line">
			<input type="text" v-model="formData.email" placeholder="邮箱" />
		</view>
		<view>
			<input type="text" v-model="formData.password" placeholder="密码" />
		</view>
		<view>
			<input type="text" v-model="formData.re_password" placeholder="确认密码" />
		</view>
		<view class="code-line">
			<input type="text" v-model="formData.email_code" placeholder="验证码" />
			<text class="code-link" @click="seedMail()">
				<text v-if="mailSeedState">获取验证码</text>
				<text v-else="">重新获取{{stataIime}}s</text>
			</text>
		</view>
		<view class="register-link">
			有账号，<navigator url="/pages/login/login" class="link-text">登录</navigator>
		</view>
		<view>
			<button class="btn" @click="register()">注&nbsp;&nbsp;&nbsp;&nbsp;册</button>
		</view>
		<view>
			<radio-group @change="fun">
				<radio value="0">男</radio>
				<radio value="1">女</radio>
			</radio-group>
			<checkbox-group>
				<checkbox></checkbox>
			</checkbox-group>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				formData : {
					app_token:'yx_third',
					email:'',
					email_code:'',
					password:'',
					re_password:'',
					name:'wenyi',
					avatar:'http://t7.baidu.com/it/u=3616242789,1098670747&fm=79&app=86&size=h300&n=0&g=4n&f=jpeg?sec=1590070656&t=893bcfd96a07c54c94e8ab916a7976d6',
					sex:0,
					telephone:'18798639484'
				},
				mailSeedState:true,
				stataIime:60
			}
		},
		methods: {
			fun:function(e){
				this.formData.sex = e.detail.value;
			},
			seedMail:function(){
				var thisObj = this;
				if(this.checkMail()){
					if(!this.mailSeedState) return;
					this.mailSeedState = false;
					this.stataIime = 60;
					var intime =  setInterval(function(){
						thisObj.stataIime--;
						if(thisObj.stataIime<=0){
							this.mailSeedState = true;
							clearInterval(intime);
						}
					},1000)
					var formData = {
						app_token:'yx_third',
						email:this.formData.email,
					};
					uni.request({
						url:'https://api.yqxbxb.com/public/api/user/third/email/code',
						data:formData,
						method:'post',
						success:function(res){
							if(res.data.success){
								uni.showModal({
									content: '验证码发送成功，请到邮箱获取验证码',
									showCancel: false
								});
							}else{
								clearInterval(intime);
								thisObj.mailSeedState = true;
								uni.showModal({
									content: '验证码发送失败，请检查邮箱格式',
									showCancel: false
								});
							}
						},
						fail:function(){
							console.log('你错了');
						}
					})
				}
			},
			register:function(){
				if(this.registerCheck()){
					var formData = this.formData;
					uni.request({
						url:'https://api.yqxbxb.com/public/api/user/third/email/register',
						data:formData,
						method:'post',
						success:function(res){
							console.log(res);
						},
						fail:function(){
							console.log('你错了');
						}
					})
				}
			},
			checkMail:function(){
				//邮箱必须输入
				if(!this.formData.email){
					uni.showModal({
						content: '邮箱不能为空',
						showCancel: false
					});
					return false;
				}
				return true;
			},
			registerCheck:function(){
				
				//邮箱必须输入
				if(!this.formData.email){
					uni.showModal({
						content: '邮箱不能为空',
						showCancel: false
					});
					return false;
				}
				//密码必须输入
				if(this.formData.password == ''){
					uni.showToast({
						title:"密码必须输入",
						icon:"none"
					})
					return false;
				}
				//邮箱验证码必须输入
				if(this.formData.email_code){
					uni.showToast({
						title:"邮箱验证码必须输入",
						icon:"none"
					})
					return false;
				}
				//两个密码一致
				if(this.formData.password != this.formData.re_password){
					uni.showToast({
						title:"两个密码一致",
						icon:"none"
					})
					return false;
				}
				return true;
			}
		}
	}
</script>

<style>
	@import url("../../static/login.css");
	.code-line input{
		width: 254upx;
		float: left;
	}
	.register-link{
		clear: both;
	}
	.code-line text{
		float: right;
		line-height: 80upx;
		color: #0055BA;
	}
	
</style>
