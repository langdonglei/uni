<template>
	<u-action-sheet :list="actionSheetList" v-model="actionSheetListIsShow"></u-action-sheet>
	
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
		}
	}
</script>
