<template>
	<view>
		<view class="logo">
			<image :src="logo_imag"></image>
		</view>

		<view class="tabs">
			<v-tabs padding="10px 20px" v-model="tab1" auto :tabs="tabs1" :lineColor="red" color="#989898" activeColor="#44dfe1"
			 fontSize="30rpx"></v-tabs>
		</view>

		<!-- 账号 -->
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
			<view class="password_taks" v-if="tab1==1">
				<input placeholder="请输入手机验证码"/>
			</view>
			<view class="password_taks" v-if="tab1==0">
				<input placeholder="请输入密码"/>
			</view>
			<view class="password_taols" v-if="tab1==1">
				<text>获取验证码</text>
			</view>
		</view>
		<!-- 滑块 -->
		
		<view>
			<xl-slider-verify @success="verifySuccess" sliderBlockBg="white" :reset="false" forntBg="#44dfe1"></xl-slider-verify>
		</view>
		
		<!-- 登录 -->
		
		<view class="btn" @click="home">
			<text>登录</text>
		</view>
	</view>
</template>

<script>
	import xlSliderVerify from '@/components/xl-slider-verify/xl-slider-verify.vue'
	export default {
		components:{
			xlSliderVerify
		},
		data() {
			return {
				
				logo_imag: '../../static/a3.jpg',
				tab1: 1,
				tabs1: ['密码登录', '验证码登录'],
				red: "#44dfe1"
			}
		},
		methods:{
			verifySuccess(){
				console.log('验证成功')
			},
			home:function(){
				uni.navigateTo({
					url:"../home/home"
				})
			}
		}
	}
</script>

<style>
	page {
		background-image: url(../../static/a4.jpg);
	}

	.logo {
		display: flex;
		justify-content: center;
		margin-top: 35rpx;
	}

	.logo image {
		width: 35%;
		height: 250rpx;
	}

	.tabs {
		margin-top: 30rpx;
	}

	.tapinput {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		border: 1px solid #565656;
		border-radius: 10rpx;
		width: 80%;
		margin-left: 10%;
		margin-top: 70rpx;
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
		margin-top: 50rpx;
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
</style>
