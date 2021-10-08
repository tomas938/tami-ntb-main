<template>
	<div class="hero">
		<vueper-slides :arrows="false" fixed-height="85vh" class="no-hover">
			<vueper-slide
				v-for="i in slides"
				:key="i"
				:image="i.image"
				:title="i.title"
				:content="i.content"
			/>
		</vueper-slides>
		<div class="hero__content">
			<h1>
				Mliečna <br />
				chuť Tatier
			</h1>
			<span> v novom dizajne</span>
		</div>
	</div>
</template>

<script>
import { VueperSlides, VueperSlide } from "vueperslides";

export default {
	components: {
		VueperSlides,
		VueperSlide,
	},
	data() {
		return {
			slides: [
				{
					image: require("../assets/Hero/bg-1.png"),
				},
				{ image: require("../assets/Hero/bg-2.png") },
				{ image: require("../assets/Hero/bg-3.png") },
			],
		};
	},
};
</script>

<style lang="scss" scoped>
.hero {
	position: relative;
	&__content {
		z-index: 1;
		position: absolute;
		top: 50%;
		left: 15%;
		transform: translateY(-50%);
		@media only screen and (max-width: 1300px) {
			top: 55%;
			left: 10%;
		}
		@media only screen and (max-width: 500px) {
			top: 50%;
			left: 7%;
		}
	}
	h1 {
		line-height: 15rem;
		font-size: 17rem;
		font-family: var(--hero-heading);
		color: white;
		text-shadow: 4px 4px 2px rgba(150, 150, 150, 1);
		@media only screen and (max-width: 900px) {
			font-size: 8rem;
			line-height: 8rem;
		}
	}
	span {
		color: var(--dark-blue);
		font-weight: bold;
		font-size: 4.8rem;
		@media only screen and (max-width: 800px) {
			font-size: 2.8rem;
		}
	}
}
</style>
