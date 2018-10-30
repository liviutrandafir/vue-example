<template>
	<div class="page-cover">
		<div class="page-cover__image">
			<img src="@/assets/cover-photo.png">
		</div>
		<div class="page-cover__bottom d-none d-sm-none d-md-block">
			<b-row  align-h="between">
				<b-col>
					<div class="cover-options">
						<b-button-group size="sm">
				      <b-button v-for="btn in buttons" :pressed.sync="btn.state" :variant="btn.variant" :key="btn.caption">
								<span v-bind:class="btn.icon"></span>
								<span>{{ btn.caption }}</span>
				      </b-button>
				    </b-button-group>
					</div>
				</b-col>
				<b-col cols="4">
					<div class="contact-section">
						<b-button size="sm" variant="primary" block>Contact Us</b-button>
					</div>
				</b-col>
			</b-row>
		</div>
		<div class="page-cover__bottom--mobile d-block d-sm-block d-md-none">
			<div class="cover-avatar">
				<div class="cover-avatar__image">
					<img src="@/assets/avatar.png">
				</div>
				<div class="cover-avatar__text">
					<div class="pagename">
						<a href="#">Every Interaction</a>
					</div>
					<div class="username">
						<a href="#">@EveryInteraction</a>
					</div>
				</div>
			</div>
			<div class="cover-contact">
				<b-button size="lg" variant="primary" block>Contact Us</b-button>
			</div>
			<div class="cover-actions">
				<button class="button-blue">
					<span class="mobile-like-icon"></span>
					<span>Liked</span>
				</button>
				<button class="button-blue">
					<span class="mobile-follow-icon"></span>
					<span>Following</span>
				</button>
				<button>
					<span class="mobile-messages-icon"></span>
					<span>Message</span>
				</button>
				<button>
					<span class="mobile-more-icon"></span>
					<span>More</span>
				</button>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'PageCover',
		data () {
	    return {
	      myToggle: false,
	      buttons: [
	        { variant: 'outline-secondary', caption: 'Liked', icon: 'like-icon-blue' },
	        { variant: 'outline-secondary', caption: 'Message', icon: 'message-icon' },
	        { variant: 'outline-secondary', caption: 'More', icon: 'dots-icon' },
	      ]
	    }
	  },
	  computed: {
	    btnStates () {
	      return this.buttons.map(btn => btn.state)
	    }
	  }
	};
</script>

<style lang="scss">
	@import "~/_variables.scss";
	@import "~/_sprite-icons.scss";

	.page-cover {

		&__image {
			max-height: 316px;
			overflow: hidden;

			img {
				width: 100%;
			}
		}

		&__bottom {
			background: #ffffff;
			padding: 10px;
			border-bottom-right-radius: 3px;
    	border-bottom-left-radius: 3px;
    	border: 1px solid #dddfe2;

    	.cover-options .btn-outline-secondary {
    		color: #4a4e58;
    		background: #f6f7f9;
				border-color: #ced0d4;
				padding: 3px 8px 5px;

				&:hover {
					background: $buttonsBg;
				}

				span {
					vertical-align: middle;
					font-weight: 700;

					&:first-child {
						margin-right: 5px;
					}
				}
    	}

			.contact-section {
				text-align: right;
			}
		}
	}

	@media (max-width: 767px) {
		.page-cover {
			margin: 0 -15px;
		}

		.page-cover__bottom--mobile {
			background: #ffffff;
			padding: 10px;
		}

		.cover-avatar {
			&__image {
				max-width: 100px;
				overflow: hidden;
				border: 1px solid #e6e6e6;
				display: inline-block;
				margin-right: 15px;
				vertical-align: middle;

				img {
					width: 100%;
				}
			}

			&__text {
				display: inline-block;
				vertical-align: middle;
				max-width: 65%;

				.pagename a {
					font-size: 30px;
					line-height: 40px;
					color: #000000;

					&:hover {
						text-decoration: none;
					}
				}

				.username a {
					font-size: 18px;
					line-height: 28px;
					color: #98949c;
				}
			}
		}

		.cover-contact {
			margin-top: 15px;

			button {
				background: $mainColor;
				border: 1px solid $mainColor;
			}
		}

		.cover-actions {
			margin-top: 15px;
			display: flex;

			button {
				flex: 1;
				background-color: transparent;
				border: none;
				text-align: center;
				color: #6a7180;

				&.button-blue {
					color: $mainColor;
				}

				&:hover {
					cursor: pointer;
				}

				span {
					display: block;
					font-weight: 700;
					background-size: 120%;
					left: 0;
					right: 0;
					margin: auto;

					&:first-child {
						margin-bottom: 10px;
					}
				}
			}
		}
	}

	@media (max-width: 375px) {

		.cover-avatar__text {
			max-width: 60%;

			.pagename a {
				font-size: 26px;
				line-height: 36px;
			}

			.username a {
				font-size: 16px;
				line-height: 26px;
			}
		}
	}

</style>