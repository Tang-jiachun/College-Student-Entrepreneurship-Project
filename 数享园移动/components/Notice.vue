<template>
  <view class="notice">
    <view class="title">{{ formattedTitle }}</view>
    <view class="divider1"></view>
    <view class="content">{{ content }}</view>
  </view>
</template>

<script>
export default {
  name: 'Notice',
  props: {
    title: {
      type: String,
      default: '最新公告',
    },
    content: {
      type: String,
      default: '这里是公告的具体内容',
    },
  },
  computed: {
    formattedTitle() {
      // 将 "最新公告" 四个字分为两行显示
      return this.title.replace(/(.{2})/, '$1\n');
    },
  },
};
</script>

<style scoped>

.notice {
  display: flex;
  justify-content: center;
  width: 100%;
}


/* 最新公告  样式 */
.title {
  width: 8%;
  height: 80rpx;
  margin-top: 20rpx;
  margin-left: 5%;
  text-align: center;
  font-size: 14rpx;
  font-weight: 550;
  line-height: 40rpx;
  display: flex;
  flex-wrap: wrap;
}

/* 分割线样式 */
.divider1 {
  width: 0.5%;
  height: 60rpx;
  margin-left: 10rpx;
  margin-top: 30rpx;
  background-color: #a6a6a6;
}

/* 公告内容 样式 */
.content {
  width: 70%;
  height: 80rpx;
  margin: 20rpx;
  line-height: 80rpx;
  font-size: 12rpx;
  font-weight: 500;
}

</style>