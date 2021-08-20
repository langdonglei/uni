<template>
	<view>
		<u-back-top :scroll-top="scrollTop"></u-back-top>
		<u-notice-bar :list="notice_list"></u-notice-bar>
		<u-toast ref="uToast" />
		<u-swiper :list="swiper_list"></u-swiper>
		<swiper>
			<swiper-item>
				<u-grid>
					<u-grid-item v-for="(item, index) in grid_list" :index="index" :key="index"
						@click="handle_grid_item_click">
						<u-icon :name="item" :size="46"></u-icon>
						<text>{{ '宫格' + (index + 1) }}</text>
					</u-grid-item>
				</u-grid>
			</swiper-item>
		</swiper>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>
		<u-divider>我也是有底线的</u-divider>

	</view>
</template>

<script>
	export default {
		onPageScroll(e) {
			this.scrollTop = e.scrollTop;
		},
		data() {
			return {
				scrollTop: 0,
				notice_list: ['通知：打雷啦~~~下雨啦~~~收衣服啦~~~'],
				swiper_list: [ //
					{
						image: 'https://cdn.uviewui.com/uview/swiper/1.jpg'
					}
				],
				grid_list: ['integral', 'kefu-ermai', 'coupon', 'gift', 'scan', 'pause-circle', 'wifi', 'email', 'list']
			}
		},
		methods: {
			handle_grid_item_click(index) {
				this.$refs.uToast.show({
					title: index,
					icon: false
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
