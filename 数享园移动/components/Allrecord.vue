<!-- Allrecord.vue -->
<template>
  <view class="allrecord">
    <view class="ActiveNum">我的活跃值</view>
    <view class="ColSwap">藏品流转记录</view>
    <view class="DailyCheck">每日签到</view>
  </view>
</template>

<script>
export default {
  name: "Allrecord",
  data() {
    return {};
  }
};
</script>

<style>
.allrecord {
  width: 80%;
  height: 300rpx;
  background-color: #cccccc;
  margin-left: 10%;
  border-radius: 8%;
}

.ActiveNum,
.ColSwap,
.DailyCheck {
	height: 80rpx;
	margin-left: 80rpx;
	margin-top: 30rpx;
	line-height: 80rpx;

}
</style>
