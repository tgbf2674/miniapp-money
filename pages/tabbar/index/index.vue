<template>
	<view>
		<view class="content">
			<tabs :data_source="recordTypeList" :value.sync="record.type"></tabs>
			<tags class="tags" :iconName='iconName' :selectedTag.sync="record.tag"></tags>
			</keybord>
		</view>
	</view>
</template>

<script>
	import tabs from "../../../components/tabs.vue"
	import tags from "../../../components/tags.vue"
	import keyborad from "../../../components/keybord.vue"
	export default {
		components: {
			tabs,
			tags,
			keyborad
		},
		data() {
			return {
				selected: false,
				iconName: [{
					name: "icon-study",
					title: "学习"
				}, {
					name: 'icon-shuidian',
					title: '水电'
				}, {
					name: 'icon-lunch',
					title: '饮食'
				}, {
					name: 'icon-shejiao',
					title: "社交"
				}, {
					name: 'icon-riyongpin',
					title: "日用品"
				},{
					name: 'icon-yule',
					title: "娱乐"
				},{
					name: 'icon-traffic',
					title: "交通"
				},{
					name: 'icon-HousingFund',
					title: "住房"
				},{
					name: 'icon-clothe',
					title: "服饰"
				},{
					name: "icon-jia-copy",
					title: "添加"
				},],
				selectedTag: "",
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
					tag: '',
					notes: '',
					type: '-',
					amount: ''
				}
			}
		},
	}
</script>

<style lang="scss">
	.content {
		display: flex;
		flex-direction: column;

		.tags {
			flex: 1;
			display: flex;
			flex-direction: column;
			justify-content: flex-end;
			margin-bottom: 5px;
		}
	}

	.iconfont {
		font-size: 25px;

		&.selected {
			color: #18B566;
		}
	}
</style>
