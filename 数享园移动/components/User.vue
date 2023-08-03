<template>
  <view class="User" @click="goToNewPage">
    <view class="UserAvatar"></view>
    <view class="UserName">
      <view class="UpperBox">{{ upperText }}</view>
      <view class="LowerBox">{{ lowerText }}</view>
    </view>
    <view class="Userenter">
      <image class="UserenterImg" src="/static/images/right.jpg"></image>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      upperText: "用户昵称", // 上部文字信息
      lowerText: "ID:12345678" // 下部文字信息
    };
  },
  
   methods: {
      goToNewPage() {
        uni.navigateTo({
          url: '/pages/UserInformation/UserInformation' // 替换为你要跳转的页面路径
        });
      }
    }
};


</script>

<style>
	
	
.User {
  display: flex;
  justify-content: space-between;
  width: 100%;
  height: 200rpx;
}

.UserAvatar {
  width: 18%;
  height: 130rpx;
  display: inline-block;
  margin-left: 10%;
  margin-top: 30rpx;
  background-color: #cccccc;
  border-radius: 150rpx;
}

.UserName {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-left: 10px;
}

.UpperBox {
  height: 50%;
  margin-top: 30rpx;
  margin-left: -60rpx;
  font-size: 35rpx;
}

.LowerBox {
  height: 50%;
  margin-left: -60rpx;
  font-size: 18rpx;
}

.Userenter {
  position: relative;
  width: 100px;
  height: 100px;

}

.UserenterImg {
  position: absolute;
  top: 50%;
  left: 70%;
  transform: translate(-40%, -50%);
  width: 30px; /* 调整img的宽度 */
  height: 30px; /* 调整img的高度 */
}
</style>
