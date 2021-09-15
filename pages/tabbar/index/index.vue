<template>
	<view class="content">
		<tabs :data_source="recordTypeList" :value.sync="record.type"></tabs>
		<view class="iconfont icon-clothe" :class="{selected:selected}"></view>
	</view>

</template>

<script>
	import tabs from "../../../components/tabs.vue"
	export default {
		components: {
			tabs
		},
		data() {
			return {
				title: '极简记账',
				recordTypeList: [{
						text: '支出',
						value: '-'
					},
					{
						text: '收入',
						value: '+'
					},
				],
				record: {
					tags: [],
					notes: '',
					type: '-'
				}
			}
		},
		onLoad() {},
		methods: {}
	}
</script>

<style lang="scss">
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.iconfont {
		font-size: 25px;

		&.selected {
			color: #18B566;
		}
	}
</style>
