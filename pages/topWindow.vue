<template>
	<view class="content">
		<view class="logo">
			<navigator class="logo" open-type="reLaunch" url="/pages/component/view/view">
				<image src="../static/logo.png"></image>
				<text>hello uni-app</text>
			</navigator>
		</view>
		<custom-tab-bar class="tab-bar" @onTabItemTap="handleTabItemTap" />
	</view>
</template>
<script>
	export default {
		methods: {
			handleTabItemTap(e) {
				uni.switchTab({
					url: '/' + e.pagePath
				})
			}
		}
	}
</script>
<style scoped lang="less">
	.content {
		height: 60px;
		padding: 0 15px;
		display: flex;
		justify-content: space-between;
		align-items: center;
		border-bottom: 1px solid #e1e1e1;
		.logo {
			display: flex;
			justify-content: space-between;
			align-items: center;
			image {
				height: 30px;
				width: 30px;
			}
			text {
				margin-left: 8px;
			}
		}
		.tab-bar {
			width: 360px;
		}
	}
</style>
