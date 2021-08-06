<template>
	<view class="tabbar">
			<view class="tab-box">
				首页
			</view>
			<view class="tab-box">
				关注
			</view>
			
			<view class="tab-box">
				<view class="iconfont iconjiahao icon-box">
					
				</view>
				
			</view>
			
			<view class="tab-box">
				消息
			</view>
			<view class="tab-box">
				我
			</view>
		</view>
</template>

<script>
	export default {
		name:"tab",
		data() {
			return {
				
			};
		}
	}
</script>

<style>

.tabbar{
	
	height: 50px;
	width: 100%;
	position: fixed;
	bottom: 0;
	left: 0;
	z-index: 20;
}

.tab-box{
	float: left;
	width: 20%;
	color: #FFFFFF;
	height: 50px;
	text-align: center;
	font-size: 20px;
	line-height: 50px;
}

.icon-box{
	
	width: 60%;
	height: 30px;
	background-color: #FFFFFF;
	color: #000000;
	line-height: 30px;
	margin: 10px 20%;
	border-radius: 5px;
	font-size: 20px;
}

</style>
