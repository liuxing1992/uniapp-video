<template>
	<view class="listRight">
		<view class="author-img">
			<image class="img" src="../static/logo.png" mode="aspectFit">

			</image>
			
			<view class="iconfont iconjiahao add" v-show="show" @click="hide"></view>
		</view>

		<view class="iconfont iconaixin right-box"  @click="changeColor" :style="color" />

		<text class="number">123</text>

		<view class="iconfont icontubiaozhizuo- right-box"  />

		<text class="number">456</text>

		<view class="iconfont iconfenxiang right-box" />
		
		<text class="number">789</text>

		<view class="around">
			<image class="img" src="../static/logo.png"></image>
		</view>


	</view>
</template>

<script>
	export default {
		props:['item'],
		name: "listRight",
		data() {
			return {
				show : true,
				color :''
			};
		},
		
		methods:{
			hide(){
				this.show = false
			},
			changeColor(){
				this.color = this.color==='' ? 'color:red'  :'' 
			},
			doubleChange(){
				this.color ='color:red;'
			}
		}
		
	}
</script>

<style>
	.listRight {

		width: 50px;
		flex-direction: column;
		display: flex;
		right: 20px;
		margin: 0 auto;
		align-items: center;

	}

	.author-img {
		width: 50px;
		height: 50px;
		border-radius: 50px;
		border: 2px solid #FFFFFF;
		position: relative;
	}

	.img {
		width: 50px;
		height: 50px;
		border-radius: 50%;
	}

	.right-box {
		width: 40px;
		height: 30px;
		line-height: 30px;
		margin-top: 10px;
		color: #FFFFFF;
		font-size: 24px;
		text-align: center;
	}

	.number {
		font-size: 12px;
		color: #999999;
		margin-top: 5px;
	}
	
	.around{
		width: 50px;
		height: 50px;
		margin-top: 12px;
		animation: rotate 1.5s linear 0.2s infinite ;
	}
	
	.add{
		width: 18px;
		height: 18px;
		border-radius: 50px;
		background-color: red;
		position: absolute;
		bottom: -9px;
		left: 16px;
		text-align: center;
		line-height: 18px;
		color: white;
		font-size: 12px;
	}
	
	@keyframes rotate{
		0%{
			transform: rotate(0deg);
		}
		100%{
			transform: rotate(360deg);
		}
	}
</style>
