<template>
  <view class="rotation-chart">
    <swiper class="swiper" :indicator-dots="true" :autoplay="true" :interval="3000" :duration="500" @change="handleSwiperChange">
      <swiper-item v-for="(slide, index) in slides" :key="index">
        <image class="slide-image" :src="slide.image"></image>
        <view class="slide-content">
          <text class="slide-title">{{ slide.title }}</text>
          <text class="slide-description">{{ slide.description }}</text>
        </view>
      </swiper-item>
    </swiper>
  </view>
</template>

<script>
export default {
  name: "RotationChart",
  data() {
    return {
      slides: [
        {
          image: "/static/RotationImage/1.jpg",     //轮播图的图片路径
          title: "Slide 1",                         //轮播图标题
          description: "This is the first slide"    //轮播图描述
        },
        {
          image: "/static/RotationImage/2.jpg",
          title: "Slide 2",
          description: "This is the second slide"
        },
        {
          image: "/static/RotationImage/3.jpg",
          title: "Slide 3",
          description: "This is the third slide"
        }
      ],
      activeIndex: 0
    };
  },
  methods: {
    handleSwiperChange(event) {
      this.activeIndex = event.detail.current;
    }
  }
};
</script>

<style>
	
.rotation-chart {
  margin-left: 10%;
  margin-top:80rpx;
  width: 80%;
  height: 800rpx;
}

.swiper {
  width: 100%;
  height: 100%;
}

.slide-image {
  width: 100%;
  height: 100%;
}

.slide-content {
  position: absolute;
  bottom: 20rpx;
  left: 20rpx;
  color: #fff;
}

.slide-title {
  font-size: 32rpx;
  font-weight: bold;
}

.slide-description {
  font-size: 28rpx;
}
</style>
