<template>
	<view class="videoPlayer">
		<video 
		
		@click="clickVideo" 
		id="myVideo" 
		loop="false" 
		:autoplay="autoplay" 
		:controls="false" 
		class="video"
			:src="video.src">

		</video>


	</view>
</template>

<script>
	
	var timer = null
	export default {

		name: "videoPlayer",
		props: ['video' , 'index'],
		data() {
			return {
				isPlay: false,
				clickCount : 0,
				autoplay : false
			};
		},

		onReady() {
			
			this.videoCon = uni.createVideoContext('myVideo', this) // 获取video上下文对象
			
		},
		
		created() {
			this.auto()
		},

		watch:{
			
			index:function(){
				console.log(index)
			}
			
		},
		methods: {
			
			auto(){
				if(this.index === 0 ){
					this.autoplay = true
					this.isPlay = true
				}
			
			},
			player() {

				this.videoCon.seek(0)
				this.videoCon.play()
				this.isPlay = true

			},

			pause() {
				if (this.isPlay) {
					this.videoCon.pause()
					this.isPlay = false
				}

			},

			resume() {

				this.videoCon.play()
				this.isPlay = true
			},

			clickVideo() {
				
				clearTimeout(timer)
				this.clickCount++
				timer = setTimeout(()=>{
					
					if(this.clickCount>=2){
						console.log('双击')
						this.$emit('follow')
						// uni.$emit('follow')
					}else{
						if (!this.isPlay) {
							this.resume()
						} else {
							this.pause()
						}
					}
					this.clickCount = 0
				} , 300)
				
			}

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
