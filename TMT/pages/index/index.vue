<template>
	<view class="content">
		<view class="navtap">
			<image :src="navimage"></image>
		</view>
		<view class="block">
			<text>
				{{block_text}}
			</text>
		</view>

		<view class="block_tak">
			<text>
				{{block_text1}}
			</text>
		</view>
		<!-- 登录按钮 -->
		
		<view class="btnsign" @click="sign">
			<text>登录</text>
		</view>
		
		<!-- 分割线 -->
		
		<view class="division">
			<image src="../../static/a2.jpg"></image>
		</view>
			
		<!-- 注册按钮 -->
		<view class="btnregi" @click="regi">
			<text>注册</text>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				navimage: "../../static/a1.jpg",
				block_text: "区块链交易",
				block_text1: "全力保障您的数字币资产安全"
			}
		},
		onLoad() {

		},
		methods: {
			sign:function(){
				uni.navigateTo({
					url:'../sigin/sigin'
				})
			},
			regi:function(){
				uni.navigateTo({
					url:"../regi/regi"
				})
			}
		}
	}
</script>

<style>
	.navtap {
		width: 100%;
	}

	.navtap image {
		width: 100%;
	}

	.block {
		display: flex;
		justify-content: center;
	}

	.block_tak {
		display: flex;
		justify-content: center;
	}

	.block_tak text {
		font-size: 30rpx;
		padding-top: 30rpx;
		color: #a9b3bd;
	}
	
	.btnsign{
		width: 90%;
		background-color: #1cd9dc;
		text-align: center;
		margin-left: 5%;
		border-radius: 50rpx;
		padding-top: 20rpx;
		padding-bottom: 20rpx;
		color: white;
		font-size: 30rpx;
		margin-top: 160rpx;
	}
	
	.btnregi{
		width: 90%;
		background-color: white;
		text-align: center;
		margin-left: 5%;
		border-radius: 50rpx;
		padding-top: 20rpx;
		padding-bottom: 20rpx;
		color: #1cd9dc;
		font-size: 30rpx;
		margin-top: 20rpx;
		border: 1px solid #1cd9dc;
	}
	
	.division{
		width: 100%;
		margin-left: 15%;
		margin-top: 20rpx;
	}
	.division image{
		width: 70%;
		height: 20rpx;
	}
</style>
