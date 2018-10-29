<template>
	<div class="page-content">
		<b-row>
			<b-col  xs="12" sm="12" md="8" lg="8" order="2" order-sm="2" order-md="1" order-lg="1">
				<NewsFeed />
			</b-col>
			<b-col  xs="12" sm="12" md="4" lg="4" order="1" order-sm="1" order-md="2" order-lg="2">
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

<style lang="scss">
	@media (max-width: 767px) {
		.page-content {
			margin: 0 -15px;
			overflow: hidden;
		}
	}
</style>