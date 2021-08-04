<template>
	<view class="videoPlayer">
		<video :autoplay="false" :loop="true" :controls="false"
			src="http://video.jishiyoo.com/1eedc49bba7b4eaebe000e3721149807/d5ab221b92c74af8976bd3c1473bfbe2-4518fe288016ee98c8783733da0e2da4-ld.mp4"
			class="video">

		</video>


	</view>
</template>

<script>
	export default {
		name: "videoPlayer",
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
						src: 'http://video.jishiyoo.com/1eedc49bba7b4eaebe000e3721149807/d5ab221b92c74af8976bd3c1473bfbe2-4518fe288016ee98c8783733da0e2da4-ld.mp4',
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
					}
				]
			};
		}
	}
</script>

<style>
	.videoPlayer {
		width: 100%;
		height: 100%;
	}

	.video {
		width: 100%;
		height: 100%;
	}
</style>
