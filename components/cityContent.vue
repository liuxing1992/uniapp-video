<template>
	<view class="cityContent">

		<view class="conlation">

			<view class="iconfont icondingwei conlation-left">
				自动定位：北京
			</view>
			<view class=" conlation-right">
				切换<text class="iconfont iconchangyongicon-"></text>
			</view>
		</view>

		<view class="video-list">
			<view class="item">
				
				<view class="video">
					<video 
					style="width: 100%;height: 100%;"
					objectFit="fill"
					src="http://video.jishiyoo.com/1eedc49bba7b4eaebe000e3721149807/d5ab221b92c74af8976bd3c1473bfbe2-4518fe288016ee98c8783733da0e2da4-ld.mp4"></video>
				</view>
				
				<view class="img" >
					<image class="image-box" src="../static/author.jpg"></image>
				</view>
			</view>
			
			<view class="item">
				
				<view class="video">
					<video 
					style="width: 100%;height: 100%;"
					objectFit="fill"
					src="http://video.jishiyoo.com/1eedc49bba7b4eaebe000e3721149807/d5ab221b92c74af8976bd3c1473bfbe2-4518fe288016ee98c8783733da0e2da4-ld.mp4"></video>
				</view>
				
				<view class="img" >
					<image class="image-box" src="../static/author.jpg"></image>
				</view>
			</view>
			
			<view class="item">
				
				<view class="video">
					<video 
					style="width: 100%;height: 100%;"
					objectFit="fill"
					src="http://video.jishiyoo.com/1eedc49bba7b4eaebe000e3721149807/d5ab221b92c74af8976bd3c1473bfbe2-4518fe288016ee98c8783733da0e2da4-ld.mp4"></video>
				</view>
				
				<view class="img" >
					<image class="image-box" src="../static/author.jpg"></image>
				</view>
			</view>
			
			<view class="item">
				
				<view class="video">
					<video 
					style="width: 100%;height: 100%;"
					objectFit="fill"
					src="http://video.jishiyoo.com/1eedc49bba7b4eaebe000e3721149807/d5ab221b92c74af8976bd3c1473bfbe2-4518fe288016ee98c8783733da0e2da4-ld.mp4"></video>
				</view>
				
				<view class="img" >
					<image class="image-box" src="../static/author.jpg"></image>
				</view>
			</view>
			
			
			<view class="item">
				
				<view class="video">
					<video 
					style="width: 100%;height: 100%;"
					objectFit="fill"
					src="http://video.jishiyoo.com/1eedc49bba7b4eaebe000e3721149807/d5ab221b92c74af8976bd3c1473bfbe2-4518fe288016ee98c8783733da0e2da4-ld.mp4"></video>
				</view>
				
				<view class="img" >
					<image class="image-box" src="../static/author.jpg"></image>
				</view>
			</view>
			
			<!-- <view class="item">
				
				<view class="video">
					<video src="http://video.jishiyoo.com/1eedc49bba7b4eaebe000e3721149807/d5ab221b92c74af8976bd3c1473bfbe2-4518fe288016ee98c8783733da0e2da4-ld.mp4"></video>
				</view>
				
				<view class="img" >
					<image src="../static/author.jpg"></image>
				</view>
			</view> -->

		</view>
	</view>
</template>

<script>
	export default {
		name: "cityContent",
		data() {
			return {

			};
		}
	}
</script>

<style>
	.cityContent {
		width: 100%;
		background: #000000;
		z-index: 18;
	}

	.conlation {
		width: 100%;
		height: 40px;
		overflow: hidden;
		color: white;
		padding-top: 70px;
		color: #999;

	}
	
	.conlation-left{
		float: left;
		font-size: 15px;
		padding-left: 15px;
	}
	
	.conlation-right{
		float: right;
		font-size: 15px;
		padding-right: 16px;
	}
	
	.video-list{
		width: 100%;
		overflow: hidden;
		background-color: #000000;
	}
	
	.item{
		width: 50%;
		float: left;
		position: relative;
	}
	
	.video{
		width: 92%;
		height: 300px;
		margin-left: 4%;
	}
	
	.img{
		position: absolute;
		bottom: 7px;
		right: 15px;
		
	}
	
	.image-box{
		width: 30px;
		height: 30px;
		border-radius: 50%;
	}
</style>
