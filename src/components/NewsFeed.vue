<template>
	<div class="news-feed">
		<StatusCard />
		<PostCard />
		<PostCard />
		<PostCard />
	</div>
</template>

<script>
	import StatusCard from '@/components/StatusCard.vue';
	import PostCard from '@/components/PostCard.vue';

	export default {
		name: 'NewsFeed',
		components: {
			StatusCard,
			PostCard,
		},
	};
</script>

<style lang="scss"></style>