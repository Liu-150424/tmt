<template>
	<view>
		<!-- 轮播图 -->
		
		<view>
			
		</view>
		
		<!-- 分类 -->
		
		<view class="classification">
			<view class="classification_left" v-for="cation in cation">
				<view>
					<image :src="cation.image"></image>
				</view>
				<text>
					{{cation.text}}
				</text>
			</view>
		</view>
		
		<!-- 滚动条 -->
		
		<view>
			
		</view>
		
		<!-- 数据 -->
		
		<view class="data">
			<view class="data_top" v-for="item in datapas">
				<view class="data_cla">
					<text>
						{{item.texta}}
					</text>
				</view>
				<view class="data_clb">
					<text>
						{{item.textb}}
					</text>
				</view>
				<view class="data_clc">
					<text>
						{{item.textc}}
					</text>
				</view>
			</view>
		</view>
		
		<!-- 阴影 -->
		
		<view class="shadow">
			
		</view>
		
		<!-- 新闻 -->
		
		<view class="journalism">
			<view class="journalism_bord">
				<view>
					<image  class="journalism_img1" src="../../static/a6.png"></image>
				</view>
				<view class="journalism_text1">
					<text>新闻资讯</text>
				</view>
				<view class="journalism_text2">
					<text>更多资讯</text>
				</view>
				<view class="journalism_img2">
					<image src="../../static/a12.png"></image>
				</view>
			</view>
		</view>
		
		
	</view>
</template>

<script>
	
	export default{
		data(){
			return{
				// 分类
				cation:[
					{
						image:"../../static/a3.jpg",
						text:"新手指导"
					},
					{
						image:"../../static/a3.jpg",
						text:"充币"
					},
					{
						image:"../../static/a3.jpg",
						text:"提币"
					},
					{
						image:"../../static/a3.jpg",
						text:"创建节点"
					}
				],
				
				// 数据
				datapas:[
					{
						texta:"BTC/USDT",
						textb:'1234.56',
						textc:'+3.35%'
					},
					{
						texta:"ETH/USDT",
						textb:'105.618',
						textc:'+3.35%'
					},
					{
						texta:"BCH/USDT",
						textb:'5.69856',
						textc:'-3.75%'
					}
				]
			}
		}
	}
	
</script>

<style>
	.classification{
		width: 100%;
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		margin-top: 50rpx;
		text-align: center;
	}
	.classification_left{
		width: 20%;
		margin-left: 5%;
	}
	.classification_left image{
		width: 60%;
		height: 60rpx;
	}
	.classification_left text{
		font-size: 25rpx;
		color: #5cc5fc;
	}
	
	
	.data{
		width: 100%;
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		margin-top: 50rpx;
		text-align: center;
	}
	.data_top{
		width: 25%;
		margin-left: 6%;
		font-size: 30rpx;
	}
	.data_clb{
		color: #09c396;
	}
	.data_clc{
		color: #09c396;
	}
	
	.shadow{
		width: 100%;
		height: 20rpx;
		background-color: #f0f0f0;
		margin-top: 25rpx;
	}
	
</style>
