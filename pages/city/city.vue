<template>
	<view class="city">
		
		<first-nav></first-nav>
		<city-content></city-content>
		<tab ></tab>
	</view>
</template>

<script>
	import tab from '../../components/tab.vue'
	import firstNav from '../../components/first-nav.vue'
	import cityContent from '../../components/cityContent.vue'
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		},
		components:{
			tab,
			firstNav,
			cityContent
		}
	}
</script>

<style>

.city{
	width: 100%;
	height: 100%;
	background-color: #000;
}
</style>
