<template>
	<view>
		<RotationChart></RotationChart>  
		<Calendar></Calendar>
		<Footer></Footer>
	</view>
</template>

<script>
import RotationChart from '@/components/Home/RotationChart.vue';
import Calendar from '@/components/Home/Calendar.vue';
import Footer from '@/components/Footer.vue';

	export default {
		components: {
			RotationChart,
			Calendar,
			Footer,
		},
		name:"Home",
		data() {
			return {
				
			};
		}
	}
</script>

<style>

</style>