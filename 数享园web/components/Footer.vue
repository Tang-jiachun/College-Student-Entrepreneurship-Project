<template>
	<view class="footer">
		<view class="element">联系我们</view>
		<view class="element">关于我们</view>
		<view class="element">版权声明</view>
		<view class="element">备案信息</view>
	</view>
</template>

<script>

export default {

};
</script>

<style>

/* 底部状态栏 */
.footer{
width: 100%;
height: 400rpx;
display: flex;
background-color:#383838;
justify-content: center;
position: fixed;
}

/* 底部状态栏内的文字 */
.element {
width: 130rpx;
height: 40rpx;
color: white;
display: inline-block;
font-size: 12rpx;
margin-top: 80rpx;
margin-left: 100rpx;
align-items: center;
justify-content: center;
position: relative;
}

.element:hover {
color: red;         /* 鼠标滑过时显示的颜色 */
}

.element::after {
content: "";
position: absolute;
bottom: -10rpx;
left: 0;
width: 80%;
height: 2px;
background-color: white;
transform: scaleX(1);
transition: transform 0.3s ease;
}

.element:hover::after {
transform: scaleX(1);
}
</style>