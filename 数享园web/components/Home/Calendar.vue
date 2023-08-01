<template>
  <view class="calendar">
    <view class="calendar-item" @click="goToActivityCalendar">
      <text class="calendar-title">活动日历</text>
    </view>
    <view class="calendar-item" @click="goToReleaseCalendar">
      <text class="calendar-title">发行日历</text>
    </view>
  </view>
</template>

<script>
export default {
  name: "Calendar",
  methods: {
    goToActivityCalendar() {
      uni.navigateTo({
        url: "/pages/activity/activity"
      });
    },
    goToReleaseCalendar() {
      uni.navigateTo({
        url: "/pages/activity/issue"
      });
    }
  }
};
</script>

<style>
	
.calendar {
  display: flex;
  align-items: center;
  padding: 20rpx;
  justify-content: center;
}

/* 活动日历及发行日历的样式 */
.calendar-item {
  width: 40%;
  height: 200rpx;
  background-color: #cccccc;
  border-radius: 15rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}

/* 文字 */
.calendar-title {
  font-size: 32rpx;
  color: #333;
}

.calendar-item + .calendar-item {
  margin-left: 20rpx;      /* 调整活动日历和发行日历之间的水平距离 */
}
</style>
