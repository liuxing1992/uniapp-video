<template>
	<view class="changeList">

		<scroll-view class="scrolly" scroll-y="true" :scroll-into-view="viewId">

			<view class="city-box">
				<view class="box">

					<view class="title">
						<icon class="iconfont icondingwei"></icon>当前城市
					</view>

					<view class="currentCity">北京</view>

				</view>

				<view class="box">
					<view class="title">
						热门城市
					</view>

					<view class="hotlist">
						<view class="item" v-for="(item , index) of list" :key="index">{{item}}</view>

					</view>


				</view>


				<view class="box-list" v-for="item in city" :key="item.initial">
					<view class="initial" :id="item.initial">
						{{item.initial}}
					</view>

					<view class="city-name" v-for="itemChild in item.list" :key ='item.initial'>
						{{itemChild.name}}
					</view>
				</view>
			</view>

		</scroll-view>




	</view>
</template>

<script>
	export default {

		props: ['city', 'letter'],
		name: "changeList",
		data() {
			return {
				viewId:'',
				list: ['深圳', '北京', '上海', '杭州', '武汉', '南昌', '西安', '宁波', '长沙', '宜春']

			};
		},
		watch: {
			letter() {
				this.viewId = this.letter
			}
		}

	}
</script>

<style>
	.changeList {
		width: 100%;
		height: 100%;
		background-color: #000000;
		z-index: 19;
	}

	.box {
		background-color: #3F536E;
		margin-top: 10px;
		padding: 5px;
	}

	.title {
		height: 40px;
		line-height: 40px;
		margin-left: 15px;
		color: #FFFFFF;
		font-size: 12px;
	}

	.currentCity {
		color: white;
		font-size: 12px;
		margin-left: 15px;
		height: 30px;
		line-height: 30px;
	}

	.hotlist {
		width: 100%;
		overflow: hidden;
	}

	.item {
		width: 30%;
		height: 25px;
		line-height: 25px;
		font-size: 15px;
		float: left;
		background-color: #333333;
		margin-left: 2.5%;
		margin-bottom: 10px;
		text-align: center;
		color: #aaaaaa;
	}

	.box-list {
		/* padding: 8px 15px; */
	}

	.initial {
		height: 25px;
		line-height: 25px;
		background-color: #000000;
		padding-left: 10px;
		color: white;
		font-size: 11px;
	}

	.city-name {
		background-color: #333333;
		height: 40px;
		line-height: 40px;
		padding-left: 10px;
		font-size: 14px;
	}
	
	.scrolly{
		width: 100%;
		height: 100%;
	}
</style>
