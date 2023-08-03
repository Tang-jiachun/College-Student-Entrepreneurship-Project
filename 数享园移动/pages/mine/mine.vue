<!-- App.vue -->
<template>
  <view>
    <User></User>
    <News></News>
    <Allrecord></Allrecord>
	<SySettings></SySettings>
  </view>
</template>

<script>
import User from '@/components/User.vue';
import News from '@/components/News.vue';
import Allrecord from '@/components/Allrecord.vue';
import SySettings from '@/components/SySettings.vue';

export default {
  components: {
    User,
    News,
    Allrecord,
	SySettings,
  }
};
</script>

<style>
/* 样式代码 */
</style>
