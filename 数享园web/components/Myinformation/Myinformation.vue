<template>
	<view>
		<Avatar></Avatar>
		<AllRecordSet/>
	</view>
</template>

<script>
import Avatar from '@/components/Myinformation/Avatar/Avatar.vue';
import AllRecordSet from '@/components/Myinformation/AllRecordSet/AllRecordSet.vue';

	export default {
		components: {
			Avatar,
			AllRecordSet,
		},
		name:"Myinformation",
		data() {
			return {
				
			};
		}
	}
</script>

<style>

</style>