<template>
	<view class="videoList">
		<view class="swiper-box">
			<swiper :vertical="true" class="swiper">
				<swiper-item class="swiper-item">
					<video-player></video-player>
				</swiper-item>
				<swiper-item class="swiper-item">
					<video-player></video-player>

				</swiper-item>
				<swiper-item class="swiper-item">
					<video-player></video-player>

				</swiper-item>
				
				<image src="../static/logo.png"></image>
			</swiper>
		</view>
	</view>
</template>

<script>
	import videoPlayer from './videoPlayer.vue'
	export default {
		name: "videoList",
		data() {
			return {

			};
		},

		components: {
			videoPlayer
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
</style>
