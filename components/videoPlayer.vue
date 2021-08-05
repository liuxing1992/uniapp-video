<template>
	<view class="videoPlayer">
		<video loop="false" :autoplay="false" :controls="false" class="video" :src="video.src">

		</video>


	</view>
</template>

<script>
	export default {

		name: "videoPlayer",
		props: ['video'],
		data() {
			return {

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
