<template>
	<view>
		<view class="top"></view>
		<notice :title="title" :content="content"></notice>
		<calendar :Activity="Activity" :issue="issue"></calendar>
		<sort></sort>
		<component v-if="activeSort === '最新上架'" :is="'Latest'"></component>
	    <component v-else-if="activeSort === '藏品置换'" :is="'Exchange'"></component>
		<component v-else-if="activeSort === '热度排行'" :is="'Hot'"></component>
		<component v-else-if="activeSort === '活跃值排行'" :is="'Active'"></component>
	</view>
</template>

<script>
	import Notice from '@/components/Notice.vue';
	import Calendar from '@/components/Calendar.vue';
	import Sort from '@/components/Sort.vue';
	import Latest from '@/components/Latest.vue';
	import Exchange from '@/components/Exchange.vue';
	import Hot from '@/components/Hot.vue';
	import Active from '@/components/Active.vue';
	export default {
		components: {
		    Notice,
			Calendar,
			Sort,
			Latest,
			Exchange,
			Hot,
			Active,
		},
		data() {
			return {
			  column: ['最新上架', '藏品置换', '热度排行', '活跃值排行'],
			  activeSort:'最新上架',  //默认选中的排序选项
			  title:"最新公告",
			  content:"这里是公告的具体内容",
			  Activity:"活动日历",
			  issue:"发行日历"
			}
		},
		methods: {
			handleSortClick(sort) {
			    this.activeSort = sort;
			}
		}
	}
</script>

<style>
	/* 顶部轮播图 */
	.top {
		width: 90%;
		height: 400rpx;
		background-color:#cccccc;
		border-radius: 10px;
		margin:auto;
	}
</style>