<template>
	<view class="back-top" :style="[show?'display:none':'display:block']">
	</view>
</template>

<script setup>
	import {
		onPageScroll
	} from '@dcloudio/uni-app';
	onPageScroll((e) => {
		console.log(e)
		scrollTop.value = e.scrollTop
	})
	import {
		ref,
		watchEffect
	} from "vue";
	const scrollTop = ref(0)
	const show = ref(false)

	const backTop = () => {

	}
</script>

<style lang="scss">
	.back-top {
		position: absolute;
		z-index: 999;
		right: 20rpx;
		bottom: 20rpx;
		width: 200rpx;
		height: 200rpx;
		background: green;
	}
</style>