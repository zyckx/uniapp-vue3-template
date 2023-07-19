<template>
	<view>
		<u-cell :title="articleInfo.title" :border="false">
			<template #icon>
				<u-avatar shape="square" size="35" src="https://cdn.uviewui.com/uview/album/1.jpg"
					customStyle="margin: -3px 5px -3px 0"></u-avatar>
			</template>

		</u-cell>
		<rich-text :nodes="articleInfo.richText">

		</rich-text>
		<comment></comment>
	</view>
</template>

<script setup>
	import {
		reactive
	} from "vue";
	import comment from '../../components/comment.vue'
	const articleInfo = reactive({
		title: '你好张三',
		richText: '<h1>我是张三</h1>'
	})
</script>

<style lang="scss">

</style>