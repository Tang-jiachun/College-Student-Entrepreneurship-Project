<template>
  <view class="background-bar" :style="{ backgroundImage: `url(${backgroundImage})` }">
    <view class="content" :style="{ justifyContent: verticalAlign }">
      <slot></slot>
    </view>
  </view>
</template>

<script>
export default {
  props: {
    backgroundImage: String,
    verticalAlign: String,
  },
};
</script>

<style scoped>
.background-bar {
  width: 80%;
  margin: auto;
  background-size: cover;
  display: flex;
  justify-content: center;
}
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
