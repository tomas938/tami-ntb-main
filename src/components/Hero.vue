<template>
	<div class="hero">
		<vueper-slides
			:touchable="false"
			:autoplay="true"
			:arrows="false"
			fixed-height="85vh"
			class="no-hover"
			:breakpoints="breakpoints"
		>
			<vueper-slide
				v-for="slide in slides"
				:key="slide"
				:image="slide.image"
				:title="slide.title"
				:content="slide.content"
			/>
		</vueper-slides>
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
			breakpoints: {
				900: {
					visibleSlides: "1",
					fixedHeight: "45vh",
				},
			},
			slides: [
				{
					image: require("../assets/Hero/bg-1.png"),
					title: "Mliečna </br> chuť Tatier",
					content: "v novom dizajne",
				},
				{
					image: require("../assets/Hero/bg-2.png"),
					title: "Mliečna </br> chuť Tatier",
					content: "ttootwooaodoaoaodaooad odoasdoaoo odao",
				},
				{ image: require("../assets/Hero/bg-3.png") },
			],
		};
	},
};
</script>
