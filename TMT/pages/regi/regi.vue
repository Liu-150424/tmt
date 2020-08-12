<template>
	<view>
		<view class="regitap">
			<image src="../../static/a7.jpg"></image>
		</view>
		<view class="tapinput">
			<view class="tapinput_image">
				<image style="width: 80%;height: 45rpx;" src="../../static/a5.png"></image>
			</view>
			<view class="tapinput_taks">
				<input  placeholder="请输入手机号"/>
			</view>
		</view>
		<!-- 验证码/密码 -->
		<view class="password">
			<view class="password_image">
				<image src="../../static/a96.png" style="width: 80%;height: 45rpx;"></image>
			</view>
			<view class="password_taks">
				<input placeholder="请输入手机验证码"/>
			</view>
			<view class="password_taols">
				<text>获取验证码</text>
			</view>
		</view>
		<view class="password">
			<view class="password_image">
				<image src="../../static/a96.png" style="width: 80%;height: 45rpx;"></image>
			</view>
			<view class="password_taks">
				<input placeholder="请设置登录密码"/>
			</view>
		</view>
		<view class="password">
			<view class="password_image">
				<image src="../../static/a96.png" style="width: 80%;height: 45rpx;"></image>
			</view>
			<view class="password_taks">
				<input placeholder="请确认登录密码"/>
			</view>
		</view>
		<view class="password">
			<view class="password_image">
				<image src="../../static/a96.png" style="width: 80%;height: 45rpx;"></image>
			</view>
			<view class="password_taks">
				<input placeholder="填写邀请码"/>
			</view>
		</view>
		<view class="btn" @click="sigin">
			<text>注册</text>
		</view>
		
		<view class="boxshow">
			
		</view>
		
		<view class="clause">
			<text>通过点击"注册"并同意我们的  </text>
			<text style="color: #1cd9dc;">服务条款。</text>
		</view>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				
			}
		},
		methods:{
			sigin:function(){
				uni.navigateTo({
					url:"../sigin/sigin"
				})
			}
		}
	}
</script>

<style>
	.regitap image{
		width: 80%;
		margin-left: 10%;
		height: 80rpx;
		margin-top: 80rpx;
	}
	.tapinput {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		border: 1px solid #565656;
		border-radius: 10rpx;
		width: 80%;
		margin-left: 10%;
		margin-top: 100rpx;
	}
	.tapinput_image{
		width: 10%;
		padding-top: 10rpx;
		padding-bottom: 10rpx;
		padding-left: 2%;
	}
	
	.tapinput_taks{
		width: 70%;
		padding-top: 10rpx;
		padding-bottom: 10rpx;
	}
	
	.password{
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		width: 80%;
		border: 1px solid #565656;
		border-radius: 10rpx;
		margin-left: 10%;
		margin-top: 30rpx;
	}
	
	.password_image{
		width: 10%;
		padding-top: 10rpx;
		padding-bottom: 10rpx;
		padding-left: 2%;
	}
	
	.password_taks{
		width: 50%;
		padding-top: 10rpx;
		padding-bottom: 10rpx;
	}
	.password_taols{
		width: 30%;
		height: 30rpx;
		font-size: 30rpx;
		background-color: #44dfe1;
		border-radius: 15rpx;
		padding-top: 15rpx;
		padding-bottom: 20rpx;
		margin-top: 5rpx;
		text-align: center;
		margin-left: 5%;
		color: white;
	}
	.btn{
		width: 80%;
		margin-left: 10%;
		text-align: center;
		margin-top: 50rpx;
		background-color: #1cd9dc;
		color: white;
		height: 60rpx;
		padding-top: 15rpx;
		padding-bottom: 15rpx;
		border-radius: 15rpx;
	}
	
	.boxshow{
		width: 80%;
		margin-left: 10%;
		background-color: #000000;
		height: 2rpx;
		margin-top: 30rpx;
	}
	.clause{
		text-align: center;
		font-size: 25rpx;
		color: #c1c1c1;
		margin-top: 15rpx;
	}
</style>
