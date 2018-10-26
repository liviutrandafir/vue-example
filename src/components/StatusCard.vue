<template>
	<div class="status-card">
		<b-card no-body>
		  <b-tabs card>
		    <b-tab active>
					<template slot="title">
						<img src="@/assets/status-icon.png">
						<span>Status</span>
					</template>
					<div class="status-card-content">
						<div class="status-card-avatar">
							<img src="@/assets/avatar.png">
						</div>
						<div class="status-card-input">
							<b-form-input type="text" placeholder="Write something on this page..."></b-form-input>
						</div>
					</div>
		    </b-tab>
		    <b-tab>
					<template slot="title">
						<img src="@/assets/addphoto-icon.png">
						<span>Photo/video</span>
					</template>
					<div class="status-card-drag">
						<h3>Drag your photo here</h3>
					</div>
		    </b-tab>
		  </b-tabs>
		</b-card>
	</div>
</template>

<script>
	export default {
		name: 'StatusCard',
	};
</script>

<style lang="scss">
	@import "~/_variables.scss";

	.status-card {
		margin-top: 15px;

		.card-header {
			padding: 5px 10px;

			ul {
				margin: 0;

				&:focus {
					outline: none;
				}
			}
		}

		.nav-link {
			padding: 3px;
			color: #365899;
			border: none;
			position: relative;

			&:hover {
				border: none;
			}
		}

		.nav-tabs .nav-link.active, .nav-tabs .nav-item.show .nav-link {
			background: none;
			border: none;
			padding: 3px;
			color: #4a4e58;
			position: relative;

			&::before {
				content: '';
				position: absolute;
				width: 0;
	      height: 0;
	      border-left: 9px solid transparent;
	      border-right: 9px solid transparent;
	      border-bottom: 9px solid rgba(0, 0, 0, 0.125);
	      left: 0;
	      right: 0;
	      margin: auto;
	      bottom: -5px;
			}

			&::after {
				content: '';
				position: absolute;
				width: 0;
	      height: 0;
	      border-left: 8px solid transparent;
	      border-right: 8px solid transparent;
	      border-bottom: 8px solid #ffffff;
	      left: 0;
	      right: 0;
	      margin: auto;
	      bottom: -5px;
			}
		}

		.status-card-content {
			display: flex;

			.status-card-avatar {
				display: inline-block;
				vertical-align: middle;
				max-width: 40px;
				overflow: hidden;

				img {
					max-width: 100%;
				}
			}

			.status-card-input {
				display: inline-block;
				vertical-align: middle;
				flex: 1;

				input {
					border: none;

					&:hover, &:focus, &:active {
						outline: none;
						border: none;
						box-shadow: none;
					}
				}
			}
		}

		.status-card-drag {
			text-align: center;
			color: $mainColor;
			border: 2px dashed $mainColor;
			padding: 10px;

			h3 {
				margin: 0;
			}
		}
	}
</style>