<template>
	<div class="sidebar-avatar">
		<div class="sidebar-avatar__image">
			<img src="@/assets/avatar.png">
		</div>
		<div class="sidebar-avatar__pagename">
			<a href="#">Every Interaction</a>
		</div>
		<div class="sidebar-avatar__username">
			<a href="#">@EveryInteraction</a>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'SidebarAvatar',
	};
</script>

<style lang="scss">
	@import "~/_variables.scss";

	.sidebar-avatar {
		margin-top: 12px;

		&__image {
			background: #ffffff;
			padding: 4px;
			border-radius: 3px;
			overflow: hidden;
			border: 1px solid #e0e1e5;

			img {
				max-width: 100%;
				border: 1px solid #e0e1e5;
			}
		}

		&__pagename {
			margin-top: 10px;

			a {
				font-size: 24px;
				line-height: 26px;
				color: #000000;

				&:hover {
					text-decoration: none;
				}
			}
		}

		&__username a {
			font-size: 14px;
			line-height: 24px;
			color: #98949c;

			&:hover {
				text-decoration: none;
			}
		}
	}

	@media (max-width: 767px) {
		.sidebar-avatar {

			&__image {
				display: inline-block !important;
				width: 40px;
			}

			&__pagename {
				margin-top: 10px;

				a {
					font-size: 24px;
					line-height: 26px;
					color: #000000;

					&:hover {
						text-decoration: none;
					}
				}
			}

			&__username a {
				font-size: 14px;
				line-height: 24px;
				color: #98949c;

				&:hover {
					text-decoration: none;
				}
			}
		}
	}
</style>