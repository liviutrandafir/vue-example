<template>
	<div class="main-header">
		<b-container>
			<b-row>
				<b-col sm="12" md="6">
					<div class="navbar-left">
						<b-navbar-brand class="d-none d-sm-none d-md-block" href="#"><img src="@/assets/logo.png"></b-navbar-brand>
						<div class="back-button d-block d-sm-block d-md-none">
							<button class="back-icon"></button>
						</div>
						<b-nav-form class="main-header__search">
							<b-form-input size="sm" class="mr-sm-2" type="text" placeholder="Every Interaction"/>
							<b-button type="submit"><span class="search-icon"></span></b-button>
						</b-nav-form>
					</div>
				</b-col>
				<b-col sm="6" class="d-none d-sm-none d-md-block">
					<div class="navbar-right">
						<div class="options-menu">
							<div class="profile-button">
								<a href="#">
									<span class="profile-button__picture"><img src="@/assets/avatar.png"></span>
									<span class="profile-button__text">Alex</span>
								</a>
							</div>
							<button class="navbar-options-button">
								<span>Home <span class="notifications">5</span></span>
							</button>
							<button class="navbar-options-button">
								<span>Create</span>
							</button>
						</div>
						<div class="notifications-menu">
							<button><span class="friends-icon"></span></button>
							<button><span class="messages-icon"></span></button>
							<button><span class="globe-icon"></span></button>
						</div>
						<div class="settings-menu">
							<button>
								<span class="lock-icon"></span>
								<span class="arrow-icon"></span>
							</button>
						</div>
					</div>
				</b-col>
			</b-row>
		</b-container>
	</div>
</template>

<script>
	export default {
		name: 'Header',
	};
</script>

<style lang="scss">
	@import "~/_variables.scss";
	@import "~/_sprite-icons.scss";

	#app .main-header {
		background-color: $mainColor !important;
		border-bottom: 1px solid #29487d;
		color: #ffffff;
		padding: 8px 0;

		.navbar-left {
			display: flex;
		}

		.navbar-brand {
			padding: 0;
			font-size: medium;
			display: inline-block;
			margin-right: 8px;
			transform: translateY(-1px);
			width: 25px;

			img {
				width: 102%;
			}
		}

		&__search {
			position: relative;
			flex: 1;

			input {
				max-height: 26px;
				border-radius: 2px;
				width: 100%;
				margin-right: 0 !important;
				border: none !important;
			}

			button {
				position: absolute;
				top: 1px;
				bottom: 1px;
				right: 0;
				padding: 0 20px;
				line-height: 12px;
				background-color: #f6f7f9;
				border: none;
				border-top-left-radius: 0;
				border-bottom-left-radius: 0;

				&:hover {
					background-color: #EBEDF0;
				}
			}
		}

		.navbar-right {
			text-align: right;
			font-size: 0;

			.options-menu {
				display: inline-block;
				vertical-align:middle;
				margin-right: 10px;

				.profile-button {
					display: inline-block;
					text-align: left;

					a   {
						color: #ffffff;
						display: block;
						line-height: 12px;
						padding-right: 5px;
						border-radius: 3px;
						font-family: $mainFont;
						font-size: 14px;

						&:hover {
							background: $buttonsBg;
							text-decoration: none;
						}
					}

					&__picture {
						width: 24px;
						height: 24px;
						display: inline-block;
						margin-right: 4px;

						img {
							max-width: 100%;
							border-radius: 2px;
							overflow: hidden;
						}
					}

					&__text {
						display: inline-block;
						padding-right: 5px;
					}
				}

				.navbar-options-button {
					background: none;
					border: none;
					color: #ffffff;
					border-radius: 3px;
					line-height: 12px;
					min-height: 26px;
					font-family: $mainFont;
					position: relative;
					font-size: 14px;


					.notifications {
						font-size: 12px;
						padding: 1px 2px;
						border-radius: 2px;
						background: rgba(0, 0, 0, .2);
					}

					&::before {
						content: '';
						position: absolute;
				    display: block;
				    height: 18px;
				    left: -1px;
				    top: 4px;
				    bottom: 4px;
				    width: 1px;
				    background: rgba(0, 0, 0, .2);
					}

					&:hover {
						background: $buttonsBg;
						text-decoration: none;
					}
				}
			}

			.notifications-menu {
				display: inline-block;
				vertical-align: middle;
				margin-right: 10px;

				button {
					background: none;
					border: none;
					line-height: 0px;
					min-height: 20px;
					padding: 5px;
					transition: 100ms ease-in-out;

					&:hover {
						opacity: 0.7;
						cursor: pointer;
					}
				}
			}

			.settings-menu {
				display: inline-block;
				vertical-align: middle;
				position: relative;

				button {
					background: none;
					border: none;
					transition: 100ms ease-in-out;

					&:hover {
						cursor: pointer;
						opacity: 0.7;
					}

					span {
						display: inline-block;
						vertical-align: middle;
						margin-left: 5px;
					}
				}

				&::before {
						content: '';
						position: absolute;
				    display: block;
				    height: 18px;
				    left: -1px;
				    top: 0px;
				    bottom: 0px;
				    width: 1px;
				    background: rgba(0, 0, 0, .2);
					}
			}
		}
	}

	@media (max-width: 767px) {
		.main-header {
			&__search {
				input {
					background: #293e6a;
					text-align: center;
					color: #ffffff !important;

					&::placeholder {
					    color: #ffffff;
					    opacity: 1;
					}

					&:hover, &:active, &:focus {
						background: #293e6a;
					}
				}

				button {
					display: none;
				}
			}

			.back-button {
				margin-right: 10px;
				max-height: 25px;

				button {
					background-color: none;
					border: none;
					max-height: 25px;
					width: 25px;
					height: 25px;
					padding: 0;
					background-size: 90%;
					background-position: 0px -0px !important;

					&:hover {
						cursor: pointer;
					}
				}
			}
		}
	}
</style>