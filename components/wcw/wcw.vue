<template>
	<view>
		<view class="article">
			<view class="article-name" v-for="item in cats":key='item.id'>
				{{item.catname}}
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props:['cats'],
		name:"wcw",
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
