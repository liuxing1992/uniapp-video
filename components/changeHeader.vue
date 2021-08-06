<template>
	<view >
		<view class="changeHeader">
			
			<view class="iconfont iconfanhui left"></view>
			
			<view class="title">切换城市</view>
			
			
		</view>
		<view class="ground"></view>
	</view>
</template>

<script>
	export default {
		name:"changeHeader",
		data() {
			return {
				
			};
		}
	}
</script>

<style>

.changeHeader{
	width: 100%;
	height: 80px;
	line-height: 80px;
	position: fixed;
	top: 0;
	left: 0;
	margin: 0 auto;
	background-color: #000000;
	
}

.left{
	position: absolute;
	top: 0;
	left: 15px;
	height: 80px;
	line-height: 80px;
	color: #FFFFFF;
	font-size: 18px;
}

.title{
	font-size: 18px;
	text-align: center;
	color: #FFFFFF;
}

.ground{
		width: 100%;
		height: 80px;
	}
</style>
