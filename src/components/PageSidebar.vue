<template>
	<div class="sidebar">
		<SidebarAvatar />
		<SidebarMenu />
	</div>
</template>

<script>
	import SidebarAvatar from '@/components/SidebarAvatar.vue';
	import SidebarMenu from '@/components/SidebarMenu.vue';

	export default {
		name: 'PageSidebar',
		components: {
	    SidebarAvatar,
	    SidebarMenu,
	  },
	};
</script>
<style lang="scss">

</style>