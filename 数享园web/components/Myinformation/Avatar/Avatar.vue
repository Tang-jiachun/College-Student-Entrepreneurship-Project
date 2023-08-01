<template>
	<view class="Avatar">
		<view class="AvatarImg">
			<image class="img" src="/static/images/avatarimg.jpg"></image>
		</view>
		<view class="UserInfo">
			<view class="UserName">用户名: {{username}}</view>
			<view class="UserId">ID: {{ID}}</view>
		</view>
		<view class="edit">
			<text>编 辑</text>
		</view>
	</view>
</template>

<script>
	export default {
		name:"Avatar",
		data() {
			return {
				username: "用户昵称",
				ID: 12345678,
			};
		}
	}
</script>

<style>
.Avatar {
	width: 80%;
	height: 400rpx;
	margin-left: 10%;
	margin-top: 150rpx;
	display: flex;
	align-items: center;
	background-color: #f1f1f1;
}

.AvatarImg {
	width: 200rpx;
	height: 200rpx;
	border-radius: 50%;
	display: flex;
	justify-content: center;
	align-items: center;
	background-color: pink;
	margin-left: 80rpx;
}

.img {
	width: 100%;
	height: 100%;
	border-radius: 50%;
}

.UserInfo {
	display: flex;
	flex-direction: column;
	justify-content: center;
	margin-left: 20px;
}

.UserName,
.UserId {
	display: inline-block;
}

.edit {
	display: flex;
	width: 150rpx;
	height: 80rpx;
	color: #4fccfa;
	justify-content: center;
	align-items: center;
	margin-left: 1500rpx;
	border: 4rpx solid #4fccfa;
	border-radius: 15%;
	background-color: white;
}
</style>
