<template>
  <view class="mydetais">
    <view class="mycol">
      <image class="myimg" src="/static/images/藏品.jpg"></image>
      <text class="mytext">我的藏品</text>
    </view>
    <view class="myconcern">
      <image class="myimg" src="/static/images/关注2.jpg"></image>
      <text class="mytext">我的关注</text>
    </view>
    <view class="mynews">
      <image class="myimg" src="/static/images/消息.jpg"></image>
      <text class="mytext">我的消息</text>
    </view>
  </view>
</template>

<style>
.mydetais {
  margin-top: 30rpx;
  display: flex;
  /* background-color: pink; */
}

.mycol,
.myconcern,
.mynews {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  width: 30%;
  height: 80rpx;
  /* background-color: pink; */
  margin-left: 2%;
}

.mycol {
	margin-left: 8%;
}
.myimg {
  width: 30px; /* 调整img的宽度 */
  height: 30px; /* 调整img的高度 */
}

.mytext {
  font-size: 18rpx;
  margin-left: 10rpx; /* 调整文字与图片之间的间距 */
}
</style>
