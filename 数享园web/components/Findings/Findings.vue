<template>
	<view>
		<Post></Post>
		<Footer></Footer>
	</view>
</template>

<script>
import Post from '@/components/Findings/Post/Post.vue';
import Footer from '@/components/Footer.vue';
	export default {
		components : {
			Footer,
			Post,
		},
		name:"Findings",
		data() {
			return {
				
			};
		}
	}
</script>

<style>

</style>