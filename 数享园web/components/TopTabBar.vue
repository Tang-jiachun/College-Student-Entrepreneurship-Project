<template>
  <view>
    <view class="toptabbar">
      <image class="appimg" src="/static/images/appimg.jpg"></image>
      <view class="apptext">数享园</view>
      <view class="tabbar" :class="{ active: activeTab === '首页' }" @click="activeTab = '首页'">首页</view>
      <view class="tabbar" :class="{ active: activeTab === '馆藏' }" @click="activeTab = '馆藏'">馆藏</view>
      <view class="tabbar" :class="{ active: activeTab === '发现' }" @click="activeTab = '发现'">发现</view>
      <view class="tabbar" :class="{ active: activeTab === '我的' }" @click="activeTab = '我的'">我的</view>
    </view>
    <view>
      <Home v-if="activeTab === '首页'" />
      <Collection v-if="activeTab === '馆藏'" />
      <Findings v-if="activeTab === '发现'" />
      <Myinformation v-if="activeTab === '我的'" />
    </view>
  </view>
</template>

<script>
import Home from '@/components/Home/Home.vue';
import Collection from '@/components/Collection/Collection.vue';
import Findings from '@/components/Findings/Findings.vue';
import Myinformation from '@/components/Myinformation/Myinformation.vue';

export default {
  name: "TopTabBar",
  components: {
    Home,
    Collection,
    Findings,
    Myinformation
  },
  data() {
    return {
      activeTab: '首页'
    };
  }
};
</script>

<style>
.toptabbar {
  display: flex;
  align-items: center;
  margin-top: 20rpx;
  margin-bottom: 50rpx;
  position: fixed;        /* 固定在页面顶部 */
  top: 0;
  left: 0;
  right: 0;
  background-color: white;
  z-index: 999; 
}

.appimg {
  width: 150rpx;
  height: 150rpx;
  margin-left: 50rpx;
  margin-top: 20rpx;
}

.tabbar {
  width: 400rpx;
  text-align: center;
  margin-left: 20rpx;
  position: relative;
}

.tabbar::after {
  content: '';
  display: block;
  margin: auto;
  width: 20%;          /* 调整下划线的宽度 */
  height: 2px;
  background-color: #000;
  position: absolute;
  bottom: -2px;
  left: 40%;           /* 调整下划线的位置 */
  opacity: 0;
  transition: opacity 0.3s;
}

.tabbar.active::after {
  opacity: 1;
}

</style>
