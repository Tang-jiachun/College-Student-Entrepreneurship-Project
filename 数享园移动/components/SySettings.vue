<template>
	<view class="sysettings">
		<view class="invite">分享邀请</view>
		<view class="settings">系统设置</view>
	</view>
</template>

<script>
	export default {
		name:"SySettings",
		data() {
			return {
				
			};
		}
	}
</script>

<style>
	
	
.sysettings{
	width: 80%;
	height: 200rpx;
	background-color: #cccccc;
	margin-top: 40rpx;
	margin-left: 10%;
	border-radius: 8%;
}


.invite,
.settings {
	height: 80rpx;
	margin-left: 80rpx;
	margin-top: 30rpx;
	line-height: 80rpx;
}
</style>