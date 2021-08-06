<template>
	<view class="changeAlphabct">
		<view class="list">
			<view 
			@touchstart="touchstart"
			@touchmove="touchmove"
			@touchend="touchend"
			hover-class="hover" class="item" v-for="item in city" @click="click(item.initial)">
				{{item.initial}}

			</view>
		</view>
	</view>
</template>

<script>
	
	var timer= null
	export default {
		props: ['city'],
		name: "changeAlphabct",
		data() {
			return {
				touch : false
			};
		},

		methods: {
			click(res) {
				this.$emit('change', res)
			},
			
			touchstart(){
				this.touch = true
			},
			touchmove(e){
				clearTimeout(timer)
				timer = setTimeout(()=>{
					
					if(this.touch){
						const touchY = e.changedTouches[0].pageY-160
						const index = Math.floor(touchY/18)
						if(index>=0 && index<this.city.length){
							this.$emit('change' , this.city[index].initial)
						}
					}
				} , 30)
				
			},
			touchend(){
				this.touch = false
			}
			
			
		}

	}
</script>

<style>
	.changeAlphabct {
		position: fixed;
		right: 0px;
		top: 150px;
		z-index: 20;

	}

	.list {
		width: 30px;
		right: 10px;

	}

	.item {
		text-align: center;
		line-height: 18px;
		font-size: 12px;
		color: white;
	}

	.hover {
		text-align: center;
		line-height: 18px;
		font-size: 16px;
		color: white;
	}
</style>
