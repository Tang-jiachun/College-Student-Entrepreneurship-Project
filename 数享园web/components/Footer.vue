<template>
  <view>
    <view class="footer">
      <view class="element">联系我们</view>
      <view class="element">关于我们</view>
      <view class="element">版权声明</view>
      <view class="element">备案信息</view>
    </view>
    <view class="contact">
      <view class="wx">微信:18176641509</view>
      <view class="qq">QQ:1073335485</view>
    </view>
  </view>
</template>

<script>
export default {

};
</script>

<style>
/* 底部状态栏 */
.footer {
  width: 100%;
  height: 200rpx;
  display: flex;
  background-color: #383838;
  justify-content: space-around;
  align-items: center;
  position: relative;
  bottom: 0;
}

/* 底部状态栏内的文字 */
.element {
  color: white;
  font-size: 12rpx;
  align-items: center;
  justify-content: center;
  position: relative;
  border-bottom: 2px solid white;   /* 添加下划线 */
  padding-bottom: 5px;              /* 调整下划线跟文字之间的距离 */
}

.element:hover {
  color: red;      /* 鼠标滑过时显示的颜色 */
}



.contact {
  height: 200rpx;
  display: flex;
  flex-direction: column;
  background-color: #383838;
}

.wx,
.qq {
  color: white;
  height: 50rpx;
  font-size: 12rpx;
  margin-left: 10%;
}
</style>
