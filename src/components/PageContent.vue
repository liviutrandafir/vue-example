<template>
	<div class="page-content">
		<b-row>
			<b-col  xs="12" sm="12" md="12" lg="8" order="2" order-sm="2" order-md="1" order-lg="1">
				<NewsFeed />
			</b-col>
			<b-col  xs="12" sm="12" md="12" lg="4" order="1" order-sm="1" order-md="2" order-lg="2">
				<WidgetSidebar />
			</b-col>
		</b-row>
		<div class="mobile-sticky-menu d-flex d-sm-flex d-md-none">
			<button><span class="m-stickybar-newsfeed-icon"></span></button>
			<button><span class="m-stickybar-friends-icon"></span></button>
			<button><span class="m-stickybar-messenger-icon"></span></button>
			<button><span class="m-stickybar-notifications-icon"></span></button>
			<button><span class="m-stickybar-more-icon"></span></button>
		</div>
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

		.mobile-sticky-menu {
			display: flex;
			position: fixed;
			left: 0;
			right: 0;
			bottom: 0;
			background: #ffffff;

			button {
				flex: 1;
				background: none;
				border: none;
				padding: 15px 5px 10px;

				span {
					background-size: 90%;
				}
			}
		}
	}
</style>