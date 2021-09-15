<template>
	<view>
		<view class="container u-skeleton">
			<view style="margin: 20px 0">
				<view v-for="(item,index) in lists" :key="index" class="lists">
					<!--u-skeleton-rect 绘制矩形-->
					<text class="u-skeleton-rect">{{item}}</text>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.container {
		padding: 20rpx 60rpx;
	}

	.lists {
		margin: 10px 0;
	}
</style>
