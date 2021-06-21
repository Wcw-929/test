<template>
	<view class="content">
		<view class="text-area">
			<wcw :cats="cats"></wcw>
		</view>
	</view>
</template>

<script>
	import wcw from '@/components/wcw/wcw.vue'
	export default {
		data() {
			return {
				cats:[]
			}
		},
		onLoad() {
			uni.request({
				url:'http://localhost:7001/cats',
				success: (res) => {
					this.cats = res.data
				}
			})
		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #333333;
	}
</style>
