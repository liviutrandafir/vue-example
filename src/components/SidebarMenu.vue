<template>
	<div class="sidebar-menu">
		<ul>
			<li><a class="active" href="#" >Home</a></li>
			<li><a href="#" >About</a></li>
			<li><a href="#" >Notes</a></li>
			<li><a href="#" >Email Signup</a></li>
			<li><a href="#" >Photos</a></li>
			<li><a href="#" >Reviews</a></li>
			<li><a href="#" >Videos</a></li>
			<li><a href="#" >Likes</a></li>
			<li><a href="#" >Posts</a></li>
		</ul>
		<div class="page-create-link">
			<b-button size="sm" variant="success">Create a page</b-button>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'SidebarMenu',
	};
</script>

<style lang="scss">
	@import "~/_variables.scss";

	.sidebar-menu {
		margin-top: 20px;

		ul {
			list-style: none;
			padding: 0;

			li {
				display: block;

				a {
					padding: 5px 10px;
					display: block;
					border-left: 3px solid $appBackground;
					color: #000000;

					&:hover, &.active {
						text-decoration: none;
						background: $buttonsBg;
						border-left: 3px solid $mainColor;
					}
				}
			}
		}
	}
</style>