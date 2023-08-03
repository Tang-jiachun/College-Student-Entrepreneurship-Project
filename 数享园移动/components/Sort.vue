<template>
  <view class="sort">
    <view class="column" :class="{ active: activeIndex === 0 }" @click="handleClick(0)">
      最新上架
    </view>
    <view class="column" :class="{ active: activeIndex === 1 }" @click="handleClick(1)">
      藏品置换
    </view>
    <view class="column" :class="{ active: activeIndex === 2 }" @click="handleClick(2)">
      热度排行
    </view>
    <view class="column" :class="{ active: activeIndex === 3 }" @click="handleClick(3)">
      活跃值排行
    </view>
  </view>
</template>

<script>
export default {
  name: 'Sort',
  data() {
    return {
      activeIndex: 0,
    };
  },
  methods: {
    handleClick(index) {
      this.activeIndex = index;
    }
  },
  props: {},
  computed: {}
};
</script>

<style>
/* 首页的四项分栏 */
.sort {
  margin-left: 5%;
  display: flex;
  justify-content: center;
}

.column {
  display: inline-block;
  width: 22%;
  height: 30px;
  /* margin-left: 10rpx; */
  margin-top: 20rpx;
  font-size: 13px;
  font-weight: 520;
  cursor: pointer;
}

/* 点击分栏，高亮显示样式 */
.active {
  font-weight: 550;
}
</style>
