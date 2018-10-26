<template>
	<div class="post-card">
		<div class="post-card__content post-content">
			<div class="post-content__avatar">
				<div class="avatar-image">
					<img src="@/assets/avatar.png">
				</div>
				<div class="avatar-text">
					<div class="avatar-username">
						<span>Every Interaction</span>
					</div>
					<div class="avatar-hours">
						<span>23h • <img src="@/assets/globe-icon-gray.png"></span>
					</div>
				</div>
			</div>
			<div class="post-content__description">
				<p>Perspective FM : #15 How to create a winning proposal with Dylan Baskind from Qwilr</p>
			</div>
			<div class="post-content__post">
				<div class="post-image">
					<img src="@/assets/post-image.png">
				</div>
				<div class="post-text">
					<div class="title">
						<h4>#15 How to create a winning proposal with Dylan Baskind from Qwilr</h4>
					</div>
					<div class="description">
						<p>This week Jon is joined by Dylan Baskind - designer/developer and founder of proposal writing tool Qwilr. We speak about Dylan's journey from working in the…</p>
					</div>
					<div class="source">
						<a href="#">PERSPECTIVE.FM</a>
					</div>
				</div>
			</div>
			<div class="post-content__options">
				<button><img src="@/assets/like-icon.png"> Like</button>
				<button><img src="@/assets/comment-icon.png"> Comment</button>
				<button><img src="@/assets/share-icon.png"> Share</button>
			</div>
		</div>
		<div class="post-card__footer">
			<div class="card-footer-avatar">
				<img src="@/assets/avatar.png">
			</div>
			<div class="card-footer-input">
				<b-form-input type="text" placeholder="Write a comment..."></b-form-input>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'PostCard',
	};
</script>

<style lang="scss">
	@import "~/_variables.scss";

	.post-card {
		margin-top: 15px;
	}

	.post-content {
		background: #ffffff;
		padding: 15px 15px 0;
		border: 1px solid #e6e6e6;

		&__avatar {

			.avatar-image {
				max-width: 40px;
				overflow: hidden;
				border: 1px solid #e6e6e6;
				display: inline-block;
				margin-right: 15px;
				vertical-align: middle;

				img {
					width: 100%;
				}
			}

			.avatar-text {
				display: inline-block;
				vertical-align: middle;

				.avatar-username {
					font-size: 14px;
					color: #365899;
					font-weight: 700;
				}

				.avatar-hours {
					font-size: 12px;
					color: #90949c;
					font-weight: 700;
				}
			}
		}

		&__description {
			margin-top: 15px;

			p {
				font-size: 16px;
				line-height: 24px;
			}
		}

		&__post {
			margin-bottom: 15px;
			border: 1px solid #e6e6e6;

			.post-image {
				max-height: 297px;
				overflow: hidden;

				img {
					width: 100%;
				}
			}

			.post-text {
				padding: 15px;

				.title h4 {
					font-size: 18px;
					line-height: 28px;
				}

				.description p {
					font-size: 14px;
					line-height: 24px;
				}

				.source a {
					font-size: 11px;
					color: #93949f;
				}
			}
		}

		&__options {
			padding: 10px 0;
			border-top: 1px solid #e6e6e6;

			button {
				border: none;
				background: none;
				font-size: 12px;
				font-weight: 700;
				color: #7f7f7f;

				&:hover {
					cursor: pointer;
				}
			}
		}
	}

	.post-card__footer {
		background: #f6f7f9;
		border: 1px solid #e6e6e6;
		border-top: none;
		padding: 15px;
		display: flex;

		.card-footer-avatar {
			display: inline-block;
			vertical-align: middle;
			max-width: 40px;
			overflow: hidden;
			border: 1px solid #e6e6e6;
			margin-right: 15px;

			img {
				width: 100%;
			}
		}

		.card-footer-input {
			display: inline-block;
			vertical-align: middle;
			position: relative;
			flex: 1;

			input {
				display: block;
				border: 1px solid #e6e6e6;
				border-radius: 2px;
				min-height: 40px;
			}
		}
	}
</style>