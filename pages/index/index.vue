<template>
	<view>
		<u-swiper :list="swiper_list"></u-swiper>
		<button @click="test">btn</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				swiper_list: [ //
					{
						image: 'https://cdn.uviewui.com/uview/swiper/1.jpg'
					}
				]
			}
		},
		methods: {
			test: function() {
				let url = '/pages/page2/page2'
				console.log(url);
				uni.switchTab({
					url: url
				})
			}
		}
	}
</script>

<style lang="scss" scoped>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
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
