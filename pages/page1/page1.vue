<template>
	<view class="content">
		<u-toast ref="uToast" />
		<swiper>
			<swiper-item>
				<u-grid>
					<u-grid-item v-for="(item, index) in list" :index="index" :key="index"
						@click="handle_grid_item_click">
						<u-icon :name="item" :size="46"></u-icon>
						<text>{{ '宫格' + (index + 1) }}</text>
					</u-grid-item>
				</u-grid>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				grid_list: ['integral', 'kefu-ermai', 'coupon', 'gift', 'scan', 'pause-circle', 'wifi', 'email', 'list'],
				isSwiper: false,
				current: 0,
				border: true,
				col: 3
			};
		},
		methods: {
			handle_grid_item_click(index) {
				this.$refs.uToast.show({
					title: index,
					icon: false
				})
			}
		}
	};
</script>

<style scoped lang="scss">
	.grid-text {
		font-size: 28rpx;
		margin-top: 4rpx;
		color: $u-type-info;
	}

	.badge-icon {
		position: absolute;
		width: 40rpx;
		height: 40rpx;
	}

	.swiper {
		height: 480rpx;
	}

	.indicator-dots {
		margin-top: 40rpx;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.indicator-dots-item {
		background-color: $u-tips-color;
		height: 6px;
		width: 6px;
		border-radius: 10px;
		margin: 0 3px;
	}

	.indicator-dots-active {
		background-color: $u-type-primary;
	}
</style>
