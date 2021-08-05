<template>
	<view class="content">
		<first-nav></first-nav>
		<vidoe-list :lists="list"></vidoe-list>
		<tab></tab>

	</view>
</template>

<script>
	import tab from '../../components/tab.vue'
	import firstNav from '../../components/first-nav.vue'
	import vidoeList from '../../components/videoList.vue'

	export default {
		components: {
			tab,
			firstNav,
			vidoeList

		},

		data() {
			return {
				title: 'Hello',
				list: []
			}
		},
		onLoad() {
			this.getVideos()
		},
		methods: {
			getVideos() {
				uni.request({
					url: 'http://localhost:80/api/videos.json',
					success: (res) => {
						console.log(res)
						this.list = res.data.list
					},
					fail() {
						console.log('fail')
					}
				})
			}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
