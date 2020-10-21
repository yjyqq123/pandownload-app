<template>
	<view>
		<!-- 自定义导航栏 -->
		<nav-bar>
			<text slot="left" class="font-md ml-3 text-white">首页</text>
			<template slot="right">
				<view
					class="flex align-center justify-center bg-icon rounded-circle mr-3"
					style="width: 60rpx; height: 60rpx;"
				>
					<text class="iconfont icon-zengjia"></text>
				</view>
				<view
					class="flex align-center justify-center bg-icon rounded-circle mr-3"
					style="width: 60rpx;height: 60rpx;"
				>
					<text class="iconfont icon-gengduo"></text>
				</view>
			</template>
		</nav-bar>
		<view class="flex" style="height: 1000px;">
			
		</view>
	</view>
</template>

<script>
import navBar from '@/components/common/nav-bar.vue';
export default {
	components: {
		navBar
	},
	data() {
		return {
			title: 'Hello'
		};
	},
	onLoad() {},
	methods: {}
};
</script>

<style>
</style>