<template>
	<view class="p-3 flex align-center border-bottom border-light-secondary">
		<text class="iconfont1" :class="iconClass"  style="font-size: 60rpx;"></text>
		<view class="flex flex-column ml-3" style="line-height: 1.2;">
			<text class="font-md">{{item.name}}</text>
			<text class="font-sm text-muted">{{item.create_time}}</text>
		</view>
		<view class="ml-auto flex align-center justify-center" style="width: 70rpx;height: 70rpx;">
			<text v-if="!item.checked" style="height: 25rpx;width: 25rpx;" class="rounded-circle border"></text>
			<text v-else class="iconfont icon-xuanze-yixuan text-primary" style="font-size: 40rpx;"></text>
			
		</view>
	</view>
</template>

<script>
	const icons = {
	  dir: {
	    icon: 'icon-file-b-0',
	    color: 'text-warning'
	  },
	  image: {
	    icon: 'icon-file-b-1',
	    color: 'text-success'
	  },
	  video: {
	    icon: 'icon-file-b-3',
	    color: 'text-primary'
	  },
	  text: {
	    icon: 'icon-file-s-1',
	    color: 'text-info'
	  },
	  none: {
	    icon: 'icon-file-b-2',
	    color: 'text-muted'
	  }
	};
	export default {
		props:{
			item: Object,
			index: [Number, String]
		},
		computed:{
			iconClass(){
				let item = icons[this.item.type];
				return `${item.icon} ${item.color}`;
			}
		}
	};
</script>

<style>
</style>
