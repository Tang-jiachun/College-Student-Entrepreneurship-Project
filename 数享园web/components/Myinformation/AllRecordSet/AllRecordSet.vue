<template>
  <view class="AllRecordSet">
    <view class="leftColumn">
      <view
        v-for="(item, index) in leftItems"
        :key="index"
        class="leftItem"
        :class="{ active: activeIndex === index }"
        @click="selectItem(index)"
      >
        {{ item }}
      </view>
    </view>
    <view class="rightColumn">
      <component :is="rightComponent"></component>
    </view>
  </view>
</template>

<script>
import mynews from '@/components/Myinformation/AllRecordSet/mynews.vue';
import myconcern from '@/components/Myinformation/AllRecordSet/myconcern.vue';
import myactive from '@/components/Myinformation/AllRecordSet/myactive.vue';
import mycollection from '@/components/Myinformation/AllRecordSet/mycollection.vue';
import colrecord from '@/components/Myinformation/AllRecordSet/colrecord.vue';
import shareinvite from '@/components/Myinformation/AllRecordSet/shareinvite.vue';
import syssettings from '@/components/Myinformation/AllRecordSet/syssetting.vue';
import logoff from '@/components/Myinformation/AllRecordSet/logoff.vue';

export default {
  name: "AllRecordSet",
  data() {
    return {
      leftItems: ["我的消息", "我的关注", "我的活跃值", "我的藏品", "藏品流转记录", "分享邀请", "系统设置","退出登录"],
      activeIndex: 0,            //默认显示左边第一栏
      rightComponent: mynews     //默认显示我的消息
    };
  },
  methods: {
    selectItem(index) {
      this.activeIndex = index;
      //根据左边点击的内容来显示右边的内容
      switch (index) {
        case 0:
          this.rightComponent = mynews;
          break;
        case 1:
          this.rightComponent = myconcern;
          break;
        case 2:
          this.rightComponent = myactive;
          break;
        case 3:
		  this.rightComponent = mycollection;
		  break;
		case 4:
		  this.rightComponent = colrecord;
		  break;
		case 5:
		  this.rightComponent = shareinvite;
		  break;
		case 6:
		  this.rightComponent = syssettings;
		  break;
		case 7:
		  this.rightComponent = logoff;
		  break;
        default:
          this.rightComponent = null;
      }
    }
  },
  components: {
    mynews,
	myconcern,
	myactive,
	mycollection,
	colrecord,
	shareinvite,
	syssettings,
	logoff,
  }
};
</script>

<style>
.AllRecordSet {
  display: flex;
  width: 100%;
  height: 100%;
  margin-top: 50rpx;
}

.leftColumn {
  flex: 0.3;   //左栏是右栏宽度的0.3倍,用于调整左右宽度比
  width: 100rpx;
  display: flex;
  flex-direction: column;
  margin-left: 10%;
  background-color: #f2f2f2;
  border-right: 50rpx solid white;   //左栏的右边框
}

/* 左栏每个内容的样式 */
.leftItem {
  height: 90rpx;
  padding: 10px;
  cursor: pointer;
  text-align: center;
}

.leftItem.active {
  background-color: #f1f1f1;
  color:#50cdfa;
}
/* 左栏鼠标滑过时的样式 */
.leftItem:hover {
  color: #50cdfa; 
}

.rightColumn {
  flex: 1;
  margin-right: 10%;
  padding: 10px;
  background-color:#f2f2f2;
}
</style>
