<template>
	<view class="videoList">
		<view class="swiper-box">
			<swiper :vertical="true" class="swiper">


				<swiper-item v-for="item of list" :key= "item.id">
					<view class="swiper-item" style="color: #555555;">
						<video-player :video = "item"></video-player>
						
					</view>
					
					<view class="left-box">
						<list-left ></list-left>
					</view>
					
					<view class="right-box">
						<list-right></list-right>
					</view>
				</swiper-item>



			</swiper>
		</view>
	</view>
</template>

<script>
	import videoPlayer from './videoPlayer.vue'
	import listLeft from './listLeft.vue'
	import listRight from './listRight.vue'
	export default {
		props:['lists'],
		name: "videoList",
		data() {
			return {
				list: [{
						id: 1,
						src: 'http://video.jishiyoo.com/1eedc49bba7b4eaebe000e3721149807/d5ab221b92c74af8976bd3c1473bfbe2-4518fe288016ee98c8783733da0e2da4-ld.mp4',
						author: "@战士",
						title: '一生独一',
						music: "@错位时空"
					},
					{
						id: 2,
						src: 'http://video.jishiyoo.com/161b9562c780479c95bbdec1a9fbebcc/8d63913b46634b069e13188b03073c09-d25c062412ee3c4a0758b1c48fc8c642-ld.mp4',
						author: "@周周珍可爱",
						title: '一对A 你们要不起 甜到你了的话请自觉双击 我要来翻牌了 @抖音小助手',
						music: "@错位时空",
					},
					{
						id: 3,
						src: 'http://video.jishiyoo.com/549ed372c9d14b029bfb0512ba879055/8e2dc540573d496cb0942273c4a4c78c-15844fe70971f715c01d57c0c6595f45-ld.mp4',
						author: "@刺客",
						title: '一生独一',
						music: "@错位时空"
					},
					{
						id: 4,
						src: 'http://video.jishiyoo.com/549ed372c9d14b029bfb0512ba879055/8e2dc540573d496cb0942273c4a4c78c-15844fe70971f715c01d57c0c6595f45-ld.mp4',
						author: "@刺客",
						title: '一生独一',
						music: "@错位时空"
					}
				]
			};
		},

		components: {
			videoPlayer,
			listLeft,
			listRight
		},
		watch:{
			lists(){
				this.list = lists
			}
		}
	}
</script>

<style>
	.videoList {
		position: fixed;
		width: 100%;
		height: 100%;
		top: 0;
		left: 0;
		background-color: #007AFF;
	}

	.swiper-box {
		width: 100%;
		height: 100%;
	}

	.swiper {
		width: 100%;
		height: 100%;
	}
	
	.swiper-item{
		width: 100%;
		height: 100%;
		z-index: 19;
	}
	
	.left-box{
		z-index: 20;
		position: absolute;
		bottom: 50px;
		left: 20px;
	}
	
	.right-box{
		z-index: 20;
		position: absolute;
		bottom: 50px;
		right: 20px;
	}
</style>
