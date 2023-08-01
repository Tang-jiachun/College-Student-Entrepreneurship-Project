<template>
  <view>
    <view class="background" :style="{ backgroundImage: `url(${backgroundImage})` }">
      <view class="text-container">
        <text class="text">数字藏品</text>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      backgroundImage: "/static/images/5.jpg"
    };
  },
  methods: {}
};
</script>

<style>
.background {
  width: 80%;
  height: 700rpx;
  margin-left: 10%;
  display: flex;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  align-items: center;             /* 垂直居中 */
  justify-content: center;         /* 水平居中 */
}

.text-container {
  display: flex;
  align-items: center;           /* 垂直居中 */
}

.text {
  color: white;
  text-align: center;
  font-size: 50px;
}
</style>
