<template>
	<div class="page-content">
		<b-row>
			<b-col cols="8">
				<NewsFeed />
			</b-col>
			<b-col cols="4">
				<WidgetSidebar />
			</b-col>
		</b-row>
	</div>
</template>

<script>
	import NewsFeed from '@/components/NewsFeed.vue';
	import WidgetSidebar from '@/components/WidgetSidebar.vue';
	export default {
		name: 'PageContent',
		components: {
			NewsFeed,
			WidgetSidebar,
		},
	};
</script>

<style lang="scss"></style>