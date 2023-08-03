<template>
  <view class="history">
    <view class="top">
      <text class="text">历史文化 类</text>
    </view>
	<view class="search" type="input" value="go to search">
		
	</view> 
  </view>
</template>

<style>
.history {
  display: flex;
  flex-direction: column;
}

.top {
  width: 100%;
  height: 330rpx;
  background-color: #cccccc;
  padding: 20px;
  display: flex;
  justify-content: center;
  align-items: flex-end;
}

.text {
  font-size: 22px;
  margin-bottom: 40rpx;
  color: #ffffff;
}

.search {
	background-color: pink;
	color: black;
}
</style>
