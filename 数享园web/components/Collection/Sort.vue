<template>
  <view class="sort">
    <view class="row">
      <view class="item" @click="goToPage1">
        <image class="item-image" src="/static/images/1.jpg"></image>
        <text class="item-text">历史文化</text>
      </view>
      <view class="item" @click="goToPage2">
        <image class="item-image" src="/static/images/2.jpg"></image>
        <text class="item-text">特色建筑</text>
      </view>
      <view class="item" @click="goToPage3">
        <image class="item-image" src="/static/images/3.jpg"></image>
        <text class="item-text">校内风景</text>
      </view>
    </view>
    <view class="row">
      <view class="item" @click="goToPage4">
        <image class="item-image" src="/static/images/4.jpg"></image>
        <text class="item-text">当代艺术</text>
      </view>
      <view class="item" @click="goToPage5">
        <image class="item-image" src="/static/images/5.jpg"></image>
        <text class="item-text">数字藏品</text>
      </view>
      <view class="item" @click="goToPage6">
        <image class="item-image" src="/static/images/6.jpg"></image>
        <text class="item-text">历史文化</text>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: "Sort",
  methods: {
    goToPage1() {
      uni.navigateTo({
      	url:"/pages/Sort/history"
      })
    },
    goToPage2() {
      uni.navigateTo({
      	url:"/pages/Sort/architecture"
      })
    },
    goToPage3() {
      uni.navigateTo({
      	url:"/pages/Sort/campus"
      })
    },
    goToPage4() {
      uni.navigateTo({
      	url:"/pages/Sort/art"
      })
    },
    goToPage5() {
      uni.navigateTo({
      	url:"/pages/Sort/digital"
      })
    },
    goToPage6() {
      uni.navigateTo({
      	url:"/pages/Sort/history"
      })
    }
  }
};
</script>

<style>
.sort {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 100rpx; 
  flex-grow: 1;
  margin-bottom: 100rpx;
}

.row {
  display: flex;
  justify-content: center;
  margin-top: 40rpx; 
}

.item {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0 20rpx; 
}

.item-image {
  width: 500rpx;
  height: 400rpx;
}

.item-text {
  margin-top: 20rpx; 
}
</style>
