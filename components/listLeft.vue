<template>
	<view class="listLeft">
		<view class="author">
			{{item.author}}
		</view>
		<view class="title">
			{{item.title}}
		</view>
		<view class="box">
			<view class="music">
				{{item.music}}
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props:['item'],
		name: "listLeft",
		data() {
			return {

			};
		}
	}
</script>

<style>

.listLeft{
	height: 150px;
	margin-left: 10px;
	color: #FFFFFF;
	width: 50%;
}
.author{
	height: 35px;
	line-height: 35px;
	font-size: 15px;	
}
.title{
	line-height: 20px;
	font-size: 12px;
	color: #FFFFFF;
	width: 100%;
}


.box{
	width: 100px;
	overflow: hidden;
}
.music{
	width: 150px;
	height: 35px;
	line-height: 35px;
	font-size: 12px;
	animation: music 4s linear 0.2s infinite;
}

@keyframes music{
	0%{
		transform: translateX(80%);
	}
	100%{
			transform: translateX(-80%);
	}
}
</style>
