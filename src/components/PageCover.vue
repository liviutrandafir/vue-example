<template>
	<div class="page-cover">
		<div class="page-cover__image">
			<img src="@/assets/cover-photo.png">
		</div>
		<div class="page-cover__bottom">
			<b-row  align-h="between">
				<b-col>
					<div class="cover-options">
						<b-button-group size="sm">
				      <b-button v-for="btn in buttons" :pressed.sync="btn.state" :variant="btn.variant" :key="btn.caption">
								<img :src="btn.icon"> {{ btn.caption }}
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
	</div>
</template>

<script>
	export default {
		name: 'PageCover',
		data () {
	    return {
	      myToggle: false,
	      buttons: [
	        { variant: 'outline-secondary', caption: 'Liked', icon: require('@/assets/like-icon-blue.png') },
	        { variant: 'outline-secondary', caption: 'Message', icon: require('@/assets/message-icon.png') },
	        { variant: 'outline-secondary', caption: 'More', icon: require('@/assets/dots-icon.png') },
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

				&:hover {
					background: $buttonsBg;
				}
    	}

			.contact-section {
				text-align: right;
			}
		}
	}
</style>