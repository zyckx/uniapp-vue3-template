<template>
	<Layout mode='zoom' show="show">
		<view class="person">
			<div class="my-bg">
			</div>
			<div class="my-card">
				<div class="person-info">
					<u-avatar text="北" fontSize="18" randomBgColor></u-avatar>
					<div class="user-name">
						星河
					</div>
					<div class="motto">
						一年精通三年熟练五年入门
					</div>
				</div>
				<div class="menu">

					<u-cell-group>
						<u-cell class="menu-item" v-for="item in menuLists" :key="item.title" :title="item.title"
							:icon="item.icon" isLink arrow-direction="right" :border="false"></u-cell>
					</u-cell-group>
				</div>
			</div>
		</view>
	</Layout>
</template>

<script setup>
	import Layout from '../../components/Layout/Layout.vue'
	import {
		reactive,
		ref
	} from "vue";
	const bgUrl = ref(`url(https://s1.ax1x.com/2023/05/04/p9tvKQf.jpg)`)
	const menuLists = reactive([{
		icon: 'search',
		title: '个人信息',
	}, {
		icon: 'search',
		title: '账号安全',
	}, {
		icon: 'search',
		title: '退出登陆',
	}])
</script>

<style lang="scss">
	.person {
		width: 100%;
		height: 100%;

		.my-bg {
			width: 100%;
			height: 500rpx;
			background: v-bind(bgUrl);
			clip-path: inset(0 -55% 0 -55% round 0 0 100% 100%);
			background-size: cover;
		}

		.my-card {
			width: 600rpx;
			margin: 0 auto;
			max-height: 100%;
			padding: 50rpx 0;
			display: flex;
			align-items: center;
			justify-content: flex-start;
			flex-direction: column;
			transform: translateY(-180rpx);
			background: #fff;
			box-shadow: 0px 0px 15px 0px rgba(0, 0, 0, 0.5);
			border-radius: 15px;

			.person-info {
				width: 400rpx;
				height: 200rpx;
				display: flex;
				justify-content: flex-start;
				align-items: center;
				flex-direction: column;
				background-color: #fff;

				.avatar {
					width: 150rpx;
					height: 150rpx;
					transform: translateY(-50rpx);
					border: 2px solid #fff;
					border-radius: 50%;
				}
			}

			.menu {
				width: 90%;
				display: flex;
				flex-direction: column;
				justify-content: center;

				.menu-item {
					display: flex;
				}
			}
		}
	}
</style>