<template>
	<view class="changeAlphabct">
		<view class="list">
			<view
			hover-class="hover"
			class="item"
			v-for="item in city"
			 @click="click(item.initial)">
				{{item.initial}}
				
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props:['city'],
		name:"changeAlphabct",
		data() {
			return {
				
			};
		},
		
		methods:{
			click(res){
				this.$emit('change' , res)
			}
		}
		
	}
</script>

<style>
.changeAlphabct{
	position: fixed;
	right: 0px;
	top: 150px;
	z-index: 20;
	
}

.list{
	width: 30px;
	right: 10px;
	
}
.item{
	text-align: center;
	line-height: 18px;
	font-size: 12px;
	color: white;
}

.hover{
	text-align: center;
	line-height: 18px;
	font-size: 16px;
	color: white;
}
</style>
