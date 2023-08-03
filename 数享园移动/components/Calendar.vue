<template>
	<view class="calendar">
		<view class="activity" 
			@click="goToActivityPage">
			{{activity}}</view>
		<view class="devider"></view>
		<view class="issue" 
			@click="goToIssuePage">
			{{issue}}</view>
	</view>
</template>


<script>
export default {
  name: 'Calendar',
  props: {
    activity: {
      type: String,
      default: '活动日历',
    },
    issue: {
      type: String,
      default: '发行日历',
    },
  },
	methods: {
		goToActivityPage() {
		uni.navigateTo({
		      url: '/pages/activity/activity'
		    });
		},
		goToIssuePage() {
		 uni.navigateTo({
		      url: '/pages/issue/issue'
		    });
		},
	},
};
</script>

<style>
	
/* 日历 */
.calendar {
	display: flex;
	justify-content: center;
}

/* 活动日历 */
.activity {
	width: 40%;
	height: 100rpx;
	text-align: center;
	font-size: 14px;
	font-weight: 540;
	line-height: 100rpx;
	border-radius: 10px;
	background-color: #cccccc;
}

/* 分隔框 */
.devider {
	width: 5px;
}

/* 发行日历 */
.issue {
	width: 40%;
	height: 100rpx;
	text-align: center;
	font-size: 14px;
	font-weight: 540;
	line-height: 100rpx;
	border-radius: 10px;
	background-color: #cccccc;
}
</style>