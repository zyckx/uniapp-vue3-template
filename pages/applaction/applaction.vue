<template>
	<view class="application">
		<div class="search">
			<u-search placeholder="日照香炉生紫烟" v-model="keyword" @search="searchSubmit"></u-search>
		</div>
		<div class="article-list">
			<u-list @scrolltolower="scrolltolower">
				<u-list-item v-for="item in articleList" :key="item.id">
					<u-cell :title="item.title" isLink :label="item.description">
						<template #icon>
							<u-avatar shape="square" size="35" src="https://cdn.uviewui.com/uview/album/1.jpg"
								customStyle="margin: -3px 5px -3px 0"></u-avatar>
						</template>
						<template #right-icon>
							<u-icon name="arrow-right"></u-icon>
						</template>
					</u-cell>
				</u-list-item>
			</u-list>
		</div>
		<u-back-top :scroll-top="scrollTop" top="50" icon="arrow-up" :iconStyle="scrollTopStyle.iconStyle"
			:customStyle="scrollTopStyle.customStyle"></u-back-top>
	</view>
</template>

<script setup>
	import {
		onLoad,
		onPageScroll
	} from '@dcloudio/uni-app'
	onLoad(() => {
		// loadmore()
	})
	onPageScroll(e => {
		scrollTop.value = e.scrollTop
		console.log(e.scrollTop)
	})
	import {
		reactive,
		ref
	} from "vue";

	const keyword = ref(null)
	const scrollTop = ref(0)
	const scrollTopStyle = reactive({
		iconStyle: {
			fontSize: '32rpx',
			color: '#2979ff'
		},
		customStyle: {
			background: 'rbga(0,0,0,0.1)',
		}
	})
	const searchSubmit = (e) => {
		console.log(e)
	}
	const articleList = ref([{
		id: 1,
		title: "我是测试标题啊",
		description: "我是介绍啊"
	}, {
		id: 2,
		title: "我是测试标题啊",
		description: "我是介绍啊"
	}, {
		id: 3,
		title: "我是测试标题啊",
		description: "我是介绍啊"
	}, {
		id: 4,
		title: "我是测试标题啊",
		description: "我是介绍啊"
	}, {
		id: 5,
		title: "我是测试标题啊",
		description: "我是介绍啊"
	}, {
		id: 6,
		title: "我是测试标题啊",
		description: "我是介绍啊"
	}, {
		id: 7,
		title: "我是测试标题啊",
		description: "我是介绍啊"
	}, {
		id: 8,
		title: "我是测试标题啊",
		description: "我是介绍啊"
	}, {
		id: 9,
		title: "我是测试标题啊",
		description: "我是介绍啊"
	}, {
		id: 10,
		title: "我是测试标题啊",
		description: "我是介绍啊"
	}, {
		id: 11,
		title: "我是测试标题啊",
		description: "我是介绍啊"
	}, {
		id: 12,
		title: "我是测试标题啊",
		description: "我是介绍啊"
	}, {
		id: 13,
		title: "我是测试标题啊",
		description: "我是介绍啊"
	}])
	const scrolltolower = () => {
		console.log('触底了')
	}
</script>

<style lang="scss">
	.application {
		position: relative;
		width: 100%;
		min-height: 100%;

		.search {
			padding: 27rpx 17rpx;
		}
	}
</style>