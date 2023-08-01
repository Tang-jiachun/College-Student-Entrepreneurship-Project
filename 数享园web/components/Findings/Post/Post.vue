<template>
  <view>
    <view class="post">
      <view
        class="postitem"
        :class="{ active: activePost === '最新动态', isActive: isActive['最新动态'] }"
        @mouseover="setActive('最新动态')"
        @click="activePost = '最新动态'"
      >
        最新动态
      </view>
      <view
        class="postitem"
        :class="{ active: activePost === '最热动态', isActive: isActive['最热动态'] }"
        @mouseover="setActive('最热动态')"
        @click="activePost = '最热动态'"
      >
        最热动态
      </view>
      <view
        class="postitem"
        :class="{ active: activePost === '我的关注', isActive: isActive['我的关注'] }"
        @mouseover="setActive('我的关注')"
        @click="activePost = '我的关注'"
      >
        我的关注
      </view>
      <view
        class="postitem"
        :class="{ active: activePost === '我的发帖', isActive: isActive['我的发帖'] }"
        @mouseover="setActive('我的发帖')"
        @click="activePost = '我的发帖'"
      >
        我的发帖
      </view>
    </view>
    <view>
      <LatestPost v-if="activePost === '最新动态'" />
      <HotPost v-if="activePost === '最热动态'" />
      <MyConcern v-if="activePost === '我的关注'" />
      <MyPost v-if="activePost === '我的发帖'" />
    </view>
  </view>
</template>

<script>
import LatestPost from '@/components/Findings/Post/LatestPost.vue';
import HotPost from '@/components/Findings/Post/HotPost.vue';
import MyConcern from '@/components/Findings/Post/MyConcern.vue';
import MyPost from '@/components/Findings/Post/MyPost.vue';

export default {
  name: "Post",
  components: {
    LatestPost,
    HotPost,
    MyConcern,
    MyPost
  },
  data() {
    return {
      activePost: '最新动态',
      isActive: {
        '最新动态': false,
        '最热动态': false,
        '我的关注': false,
        '我的发帖': false
      }
    };
  },
  methods: {
    setActive(post) {
      for (let key in this.isActive) {
        this.isActive[key] = key === post;
      }
    }
  }
};
</script>

<style>
.post {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: -10rpx;
  width: 100%;
}

.postitem {
  width: 400rpx;
  display: inline-block;
  text-align: center;
  margin-top: 120rpx;
  margin-bottom: 100rpx;
  margin-left: 20rpx;
}

.postitem.isActive {
  color: #50cdfa;      /* 设置活动状态下的文字颜色 */
}
</style>
