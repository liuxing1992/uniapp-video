<template>
	<view class="listRight">
		<view class="author-img">
			<image class="img" src="../static/bili.png" mode="aspectFit">

			</image>
		</view>
		
		<image class="right-box" />
		
		<text class="number">123</text>

		<image class="right-box" />

		<text class="number">评论</text>

		<image class="right-box" />
		<text class="number">分享</text>
		
		<view class="round">
			<image class="img" src="../static/logo.png"></image>
		</view>


	</view>
</template>

<script>
	export default {
		name: "listRight",
		data() {
			return {

			};
		}
	}
</script>

<style>

.listRight{
	
	width: 50px;
	flex-direction: column;
	display: flex;
	right: 20px;
	margin: 0 auto;
}

.img{
	width: 50px;
	height: 50px;
	border-radius: 50%;
}
</style>
