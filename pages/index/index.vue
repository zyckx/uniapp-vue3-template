<template>
	<Layout mode='zoom' show="show">
		<view class="content">
			<image class="logo" src="/static/logo.png"></image>
			<view class="text-area">
				<u-alert :title="title" type="primary"></u-alert>
			</view>
		</view>
	</Layout>
</template>

<script setup>
	import {
		ref
	} from "vue";
	import Layout from '../../components/Layout/Layout.vue'
	const title = ref('天下万般兵刃，唯有过往伤人最深——亚索', )
</script>

<style>
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
		justify-content: space-between;
		flex-direction: column;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>