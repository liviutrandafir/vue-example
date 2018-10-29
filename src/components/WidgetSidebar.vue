<template>
	<div class="widget-sidebar">
		<div class="profile-type-widget">
			<b-row>
				<b-col cols="12" order="2" order-sm="2" order-md="1" order-lg="1">
					<div class="profile-type-widget__text">
						<span>Business service • London, United Kingdom</span>
					</div>
				</b-col>
				<b-col cols="12" order="1" order-sm="1" order-md="2" order-lg="2">
					<star-rating class="stars-rating" v-bind:star-size="20" active-color="#4080ff"></star-rating>
				</b-col>
			</b-row>
		</div>
		<div class="search-widget">
			<b-form-input size="sm" class="mr-sm-2" type="text" placeholder="Search for posts on this page..."/>
			<b-button type="submit"><img src="@/assets/search-icon.png"></b-button>
		</div>
		<div class="about-widget">
			<div class="about-widget__header">
				<h4>About</h4>
			</div>
			<div class="about-widget__content">
				<div class="about-widget-map">
					<iframe src="https://www.google.com/maps/embed?pb=!1m10!1m8!1m3!1d11395.557626082405!2d26.017107300000003!3d44.43543075!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sen!2sro!4v1540538531429" width="600" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>
				</div>
				<div class="about-widget-text">
					<div class="address">
						<span class="icon"><img src="@/assets/address-icon.png"></span><span class="text">Metal Box Factory, 30 Great Guildford St      Save
SE1 0HS London</span>
					</div>
					<div class="phone">
						<span class="icon"><img src="@/assets/phone-icon.png"></span><span class="text">020 3514 0659</span>
					</div>
					<div class="ask">
						<a href="#">
							<span class="icon"><img src="@/assets/ask-icon.png"></span><span class="text">Ask for Every Interaction’s hours</span>
						</a>
					</div>
					<div class="website">
						<a href="#">
							<span class="icon"><img src="@/assets/website-icon.png"></span><span class="text">http://ww.everyinteraction.com/</span>
						</a>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
	import StarRating from 'vue-star-rating'

	export default {
		name: 'WidgetSidebar',
		component: {
			StarRating,
		},
	};
</script>

<style lang="scss">
	@import "~/_variables.scss";
	@import "~/_mixins.scss";

	.profile-type-widget {
		@include widget-card;

		&__text {
			font-size: 12px;
			color: #1d2129;
			font-weight: 700;
			margin-bottom: 5px;
		}
	}

	.search-widget {
		margin-top: 15px;
		position: relative;

		input {
			min-height: 40px;
			border-radius: 2px;
			padding-left: 35px;
		}

		button {
			background: none;
			border: none;
			position: absolute;
			top: 0;
			bottom: 0;
			left: 0;

			&:hover {
				background: none;
				border: none;
			}
		}
	}

	.about-widget {
		margin-top: 15px;

		&__header {
			@include widget-header;
		}

		&__content {
			border: 1px solid #d0d1d5;
			border-top: none;

			.about-widget-map iframe {
				width: 100%;
				height: 100px;
			}

			.about-widget-text {
				padding: 15px;
				background: #ffffff;

				.address {
					@include about-text-section(#36589f);
				}

				.phone {
					@include about-text-section(#4b4f56);
				}

				.ask {
					@include about-text-section(#4080ff);
				}

				.website {
					@include about-text-section(#36589f);
				}
			}
		}
	}

	@media (max-width: 767px) {
		.profile-type-widget {
			margin-top: 0;
			text-align: center;
			border-right: none;
			border-left: none;

			&__text {
				margin-bottom: 5px;
			}

			.stars-rating {
				margin-bottom: 15px;

				& > div {
					left: 0;
					right: 0;
					margin: auto;
				}
			}
		}
	}
</style>