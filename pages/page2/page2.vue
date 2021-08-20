<template>
	<view class="content">
		<u-grid>

			<u-grid-item @click="handle_grid_item_click">
				<u-icon name="photo" size="46"></u-icon>
				<text>图片</text>
			</u-grid-item>

			<u-grid-item :index="1">
				<u-icon name="lock" :size="46"></u-icon>
				<view class="grid-text">锁头</view>
			</u-grid-item>

			<u-grid-item :index="2">
				<u-icon name="hourglass" :size="46"></u-icon>
				<view class="grid-text">沙漏</view>
			</u-grid-item>

			<u-grid-item :index="3">
				<u-icon name="home" :size="46"></u-icon>
				<view class="grid-text">首页</view>
			</u-grid-item>

			<u-grid-item :index="4">
				<u-icon name="star" :size="46"></u-icon>
				<view class="grid-text">星星</view>
			</u-grid-item>

			<u-grid-item :index="5">
				<u-icon name="volume-up" :size="46"></u-icon>
				<view class="grid-text">音量</view>
			</u-grid-item>

			<u-grid-item :index="6">
				<u-icon name="trash" :size="46"></u-icon>
				<view class="grid-text">回收站</view>
			</u-grid-item>

			<u-grid-item :index="7">
				<u-icon name="rewind-right" :size="46"></u-icon>
				<view class="grid-text">快进</view>
			</u-grid-item>

			<u-grid-item :index="8">
				<u-icon name="shopping-cart" :size="46"></u-icon>
				<view class="grid-text">购物车</view>
			</u-grid-item>

		</u-grid>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				actionSheetList: [ //
					{
						text: '点赞',
						color: 'blue',
						fontSize: 28
					},
					{
						text: '分享'
					},
					{
						text: '评论'
					},
				],
				actionSheetListIsShow: false
			}
		},
		methods:{
			handle_grid_item_click:function(e,a,b){
				console.log(e,a,b);
			}
		}
	}
</script>

<style scoped lang="scss">
	.content {
		image {
			width: 34rpx;
			heigh: 34rpx;
			top: 14rpx;
			right: 40rpx;
		}
	}
</style>
