<template>
  <view class="home">
    <view class="header"></view>
    <view class="container">
      <view class="row">
        <view class="item" @click="handleItemClick('历史文化类')">
          <view class="item-content">
            <text class="item-text">历史文化类</text>
          </view>
        </view>
        <view class="item" @click="handleItemClick('特色建筑类')">
          <view class="item-content">
            <text class="item-text">特色建筑类</text>
          </view>
        </view>
      </view>
      <view class="row">
        <view class="item" @click="handleItemClick('校内风景类')">
          <view class="item-content">
            <text class="item-text">校内风景类</text>
          </view>
        </view>
        <view class="item" @click="handleItemClick('当代艺术类')">
          <view class="item-content">
            <text class="item-text">当代艺术类</text>
          </view>
        </view>
      </view>
      <view class="row">
        <view class="item" @click="handleItemClick('数字藏品')">
          <view class="item-content">
            <text class="item-text">数字藏品</text>
          </view>
        </view>
        <view class="item" @click="handleItemClick('历史文化类')">
          <view class="item-content">
            <text class="item-text">历史文化类</text>
          </view>
        </view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {

    };
  },
  methods: {
    handleItemClick(category) {
      // 在这里处理点击事件，根据不同的分类跳转到不同的页面
      switch (category) {
        case '历史文化类':
          uni.navigateTo({
            url: '/pages/history/history'
          });
          break;
        case '特色建筑类':
          uni.navigateTo({
            url: '/pages/architecture/architecture'
          });
          break;
        case '校内风景类':
          uni.navigateTo({
            url: '/pages/campus/campus'
          });
          break;
        case '当代艺术类':
          uni.navigateTo({
            url: '/pages/art/art'
          });
          break;
        case '数字藏品':
          uni.navigateTo({
            url: '/pages/digital/digital'
          });
          break;
        default:
          break;
      }
    }
  }
}
</script>

<style>
.header {
  margin-left: 60px;
  /* margin-top: 15px; */
  font-size: 18px;
  font-weight: 540;
}

.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: -30px;
  padding: 60px;
}

.row {
  display: flex;
  justify-content: space-between;
  width: 100%;
  margin-bottom: 100rpx;
}

.item {
  width: calc(50% - 50rpx);
  height: 190rpx;
  background-color: #cccccc;
  cursor: pointer;
  /* 添加鼠标指针样式 */
}

.item-content {
  position: relative;
  padding: 20rpx;
}

.item-text {
  color: #181819;
  position: absolute;
  bottom: -200rpx;
  font-size: 12px;
  left: 0;
  width: 100%;
  text-align: center;
}
</style>