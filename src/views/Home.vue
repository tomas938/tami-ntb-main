<template>
	<Navigation></Navigation>
	<hero></hero>
	<section class="news">
		<img
			v-if="width > 800"
			class="milk-bg"
			src="../assets/News/milk.png"
			alt="milk-background"
		/>
		<SectionDescription>
			<template v-slot:title>
				Sledujte naše
			</template>
			<template v-slot:BigTitle>
				Tami aktuality
			</template>
		</SectionDescription>
		<div class="container">
			<BigCards :data="actualityContent"></BigCards>
		</div>
		<div class="actuality">
			<ExpandButton>Všetky recepty</ExpandButton>
		</div>
	</section>
	<section class="offers">
		<SectionDescription>
			<template v-slot:title>
				školské mlieko
			</template>
			<template v-slot:BigTitle>
				Tatranskej mliekarne
			</template>
			<template v-slot:description>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex, iste odit!
				Nam consequuntur eveniet fugiat incidunt facere ea expedita mollitia ad
				laudantium magni vero porro iure perferendis ratione eum recusandae
				aliquam facilis ipsum, delectus consectetur in autem alias. Ab iste
				doloremque ullam illo voluptatibus dolorum rem sequi temporibus ex
				provident!
			</template>
		</SectionDescription>
		<div class="container">
			<OfferItems></OfferItems>
		</div>
	</section>
	<section class="catalog">
		<div class="catalog__content">
			<span>prelistujte si </span>
			<h2>Katalóg produktov</h2>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex, iste odit!
				Nam consequuntur eveniet fugiat incidunt facere ea expedita mollitia ad
				laudantium magni vero porro iure perferendis ratione eum recusandae
				aliquam facilis ipsum, delectus consectetur in autem alias.
			</p>
		</div>
		<div class="catalog__button">
			<img src="../assets/Home-page/catalog-icon.png" alt="catalog-icon" />
			<p>otvoriť Katalóg</p>
			<img
				class="catalog-bg"
				src="../assets/Home-page/catalog-bg2.png"
				alt="catalog"
			/>
			<img
				class="catalog-bg2"
				src="../assets/Home-page/catalog-bg.png"
				alt="catalog"
			/>
		</div>
	</section>
	<section class="small-carousel container">
		<SectionDescription>
			<template v-slot:title>
				kategórie
			</template>
			<template v-slot:BigTitle>
				Našich produktov
			</template>
			<template v-slot:description>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex, iste odit!
				Nam consequuntur eveniet fugiat incidunt facere ea expedita mollitia ad
				laudantium magni vero porro iure perferendis ratione eum recusandae
				aliquam facilis ipsum, delectus consectetur in autem alias. Ab iste
				doloremque ullam illo voluptatibus dolorum rem sequi temporibus ex
				provident!
			</template>
		</SectionDescription>
		<vueper-slides
			:breakpoints="breakpoints"
			class="no-shadow"
			:visible-slides="3"
			:slide-ratio="1 / 4"
			:gap="3"
			:bullets="false"
			:initSlide="2"
		>
			<template #arrow-left>
				<i @click="prevSlide" class="fas fa-chevron-left fa-1x"></i>
			</template>
			<template #arrow-right>
				<i @click="nextSlide" class="fas fa-chevron-right fa-1x"></i>
			</template>
			<vueper-slide
				v-for="(slide, index) in slides"
				:key="index"
				:title="slide.title"
				:image="slide.image"
			></vueper-slide>
		</vueper-slides>
		<Expand-button class="category">Všetky kategórie</Expand-button>
	</section>
	<section class="about">
		<div class="container">
			<AboutItems :aboutConent="aboutConent"></AboutItems>
		</div>
	</section>
	<section class="recipes">
		<img
			v-if="width > 800"
			class="milk-bg"
			src="../assets/News/milk.png"
			alt="milk-background"
		/>
		<SectionDescription>
			<template v-slot:title>
				vyskúšajte
			</template>
			<template v-slot:BigTitle>
				Recepty z našej kuchyne
			</template>
			<template v-slot:description>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex, iste odit!
				Nam consequuntur eveniet fugiat incidunt facere ea expedita mollitia ad
				laudantium magni vero porro iure perferendis ratione eum recusandae
				aliquam facilis ipsum, delectus consectetur in autem alias. Ab iste
				doloremque ullam illo voluptatibus dolorum rem sequi temporibus ex
				provident!
			</template>
		</SectionDescription>
		<div class="container">
			<BigCards :data="recipesContent"></BigCards>
		</div>
	</section>
	<Footer></Footer>
</template>

<script>
import Navigation from "../components/Navigation.vue";
import Hero from "../components/Hero.vue";
import BigCards from "../components/BigCards.vue";
import ExpandButton from "../components/ExpandButton.vue";
import SectionDescription from "../components/SectionDescription.vue";
import OfferItems from "../components/OfferItems.vue";
import Footer from "../components/Footer.vue";
import AboutItems from "../components/AboutItems.vue";
// Carousel library //
import { VueperSlides, VueperSlide } from "vueperslides";
import "vueperslides/dist/vueperslides.css";
export default {
	name: "Home",
	components: {
		Hero,
		Navigation,
		BigCards,
		ExpandButton,
		SectionDescription,
		OfferItems,
		Footer,
		AboutItems,
		VueperSlides,
		VueperSlide,
	},
	data() {
		return {
			breakpoints: {
				900: {
					visibleSlides: "2",
					fixedHeight: "300px",
				},
				600: {
					visibleSlides: "1",
					fixedHeight: "300px",
				},
			},
			width: null,
			aboutConent: [
				{
					img: "leaf",
					characteristic: "kvalitné",
					textColor: "green",
					title: "Bio výrobky",
					description:
						"Lorem ipsum dolor sit amet consectetur adipisicing elit. Consectetur quis ea accusantium laborum tempore, nulla nostrum reiciendis qui nam perspiciatis unde culpa dolore temporibus facere maiores. Nisi necessitatibus inventore vel consectetur magnam veniam incidunt non.Pariatur nemo quidem, rerum ut mollitia quas quia eligendi, quaerat molestias temporibus voluptatem, unde illo.",
				},
				{
					img: "cow",
					characteristic: "kvalitné",
					textColor: "blue",
					title: "Zariadenie",
					description:
						"Lorem ipsum dolor sit amet consectetur adipisicing elit. Consectetur quis ea accusantium laborum tempore, nulla nostrum reiciendis qui nam perspiciatis unde culpa dolore temporibus facere maiores. Nisi necessitatibus inventore vel consectetur magnam veniam incidunt non.Pariatur nemo quidem, rerum ut mollitia quas quia eligendi, quaerat molestias temporibus voluptatem, unde illo.",
				},
				{
					img: "certificate",
					characteristic: "kvalitné",
					textColor: "red",
					title: "Certifikáty",
					description:
						"Lorem ipsum dolor sit amet consectetur adipisicing elit. Consectetur quis ea accusantium laborum tempore, nulla nostrum reiciendis qui nam perspiciatis unde culpa dolore temporibus facere maiores. Nisi necessitatibus inventore vel consectetur magnam veniam incidunt non.Pariatur nemo quidem, rerum ut mollitia quas quia eligendi, quaerat molestias temporibus voluptatem, unde illo.",
				},
			],
			actualityContent: [
				{
					img: "img-1",
					heading: "Intolerancia nie je prekážkou",
					folder: "News",

					description:
						"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Labore cupiditate veniam rem ducimus obcaecati nostrum accusamus ad soluta repellendus illo!",
				},
				{
					img: "img-2",
					heading: "Intolerancia nie je prekážkou",
					folder: "News",

					description:
						"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Labore cupiditate veniam rem ducimus obcaecati nostrum accusamus ad soluta repellendus illo!",
				},
				{
					img: "img-3",
					heading: "Intolerancia nie je prekážkou",
					folder: "News",
					description:
						"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Labore cupiditate veniam rem ducimus obcaecati nostrum accusamus ad soluta repellendus illo!",
				},
			],
			recipesContent: [
				{
					img: "recipe-1",
					heading: "zemiakové pečivo s plesňovým syrom",
					folder: "recipes",
					description:
						"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Labore cupiditate veniam rem ducimus obcaecati nostrum accusamus ad soluta repellendus illo!",
				},
				{
					img: "recipe-2",
					heading: "kuracie rezne s plesňovým syrom",
					folder: "recipes",
					description:
						"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Labore cupiditate veniam rem ducimus obcaecati nostrum accusamus ad soluta repellendus illo!",
				},
				{
					img: "recipe-3",
					heading: "tortičky s plesňového syra encíán",
					folder: "recipes",
					description:
						"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Labore cupiditate veniam rem ducimus obcaecati nostrum accusamus ad soluta repellendus illo!",
				},
			],
			slides: [
				{
					title: "Mlieko",
					image: require("../assets/small-carousel/img-1.png"),
				},
				{
					title: "smotana",
					image: require("../assets/small-carousel/img-2.png"),
				},
				{
					title: "kyslomliečne výrobky",
					image: require("../assets/small-carousel/img-3.png"),
				},
				{
					title: "Syry",
					image: require("../assets/small-carousel/img-4.png"),
				},
				{
					title: "Mlieko",
					image: require("../assets/small-carousel/img-1.png"),
				},
				{
					title: "smotana",
					image: require("../assets/small-carousel/img-2.png"),
				},
				{
					title: "kyslomliečne výrobky",
					image: require("../assets/small-carousel/img-3.png"),
				},
				{
					title: "syry",
					image: require("../assets/small-carousel/img-4.png"),
				},
			],
		};
	},
	methods: {},
	mounted() {
		this.width = window.innerWidth;
		console.log(this.width);
	},
};
</script>
<style lang="scss">
.news {
	background-color: var(--news-bg);
	text-align: center;
	padding-bottom: 7rem;
	position: relative;
	.milk-bg {
		max-width: 250rem;
		position: absolute;
		width: 100%;
		top: 27%;
		left: 50%;
		transform: translateX(-50%);
		z-index: 1;
	}
	.actuality {
		display: flex;
		justify-content: center;
	}
}
.offers {
	text-align: center;
}

.catalog {
	display: flex;
	align-items: center;
	justify-content: center;
	gap: 17rem;
	position: relative;
	z-index: 0;
	padding-top: 6rem;
	padding-bottom: 7rem;
	@media only screen and (max-width: 800px) {
		flex-direction: column;
		gap: 14rem;
	}
	@media only screen and (max-width: 500px) {
		gap: 10rem;
	}
	&__content {
		max-width: 80rem;
	}
	&__button {
		position: relative;
		cursor: pointer;
		width: 26rem;
		padding: 2rem 3rem;
		letter-spacing: 0.11rem;
		display: flex;
		align-items: center;
		justify-content: center;
		gap: 2rem;
		background-color: var(--danger);
		font-family: var(--myriad-pro);
		text-transform: uppercase;
		white-space: nowrap;
		transition: 0.2s background-color ease-in-out;
		&:hover {
			background-color: rgb(233, 60, 74);
			transition: 0.2s background-color ease-in-out;
		}
		img {
			width: 2rem;
			height: 1.4rem;
		}
	}
	.catalog-bg,
	.catalog-bg2 {
		pointer-events: none;
		height: 38rem;
		width: 36rem;
		position: absolute;
		z-index: -1;
		@media only screen and (max-width: 800px) {
			max-height: 25rem;
			max-width: 23rem;
		}
		@media only screen and (max-width: 500px) {
			max-height: 18rem;
			max-width: 16rem;
		}
	}

	h2,
	p {
		color: white;
		max-width: 72rem;
	}
	h2 {
		padding-top: 2rem;
		padding-bottom: 3rem;
		font-size: 4.8rem;
	}

	span {
		font-weight: 800;
		color: var(--catalog-span);
		text-transform: uppercase;
	}
}
.recipes {
	position: relative;
	text-align: center;
	h2 {
		color: #fff;
	}

	p,
	.intro {
		color: var(--recipes-text-color);
	}
	.milk-bg {
		max-width: 250rem;
		position: absolute;
		width: 100%;
		left: 50%;
		transform: translateX(-50%);
		top: 33%;
		z-index: 1;
	}
}
.catalog,
.recipes {
	background: -moz-radial-gradient(
		circle at 50% 50%,
		rgb(80, 134, 255) 0%,
		rgb(14, 37, 91) 100%
	);
	/* safari 5.1+,chrome 10+ */
	background: -webkit-radial-gradient(
		circle at 50% 50%,
		rgb(80, 134, 255) 0%,
		rgb(14, 37, 91) 100%
	);
	/* opera 11.10+ */
	background: -o-radial-gradient(
		circle at 50% 50%,
		rgb(80, 134, 255) 0%,
		rgb(14, 37, 91) 100%
	);
	/* ie 10+ */
	background: -ms-radial-gradient(
		circle at 50% 50%,
		rgb(80, 134, 255) 0%,
		rgb(14, 37, 91) 100%
	);
	/* global 92%+ browsers support */
	background: radial-gradient(
		circle at 50% 50%,
		rgb(80, 134, 255) 0%,
		rgb(14, 37, 91) 100%
	);
}
.about {
	background-color: var(--news-bg);
}
.small-carousel {
	padding: 8rem;
	text-align: center;
	@media only screen and (max-width: 600px) {
		padding: 8rem 3rem;
	}
}
.category {
	margin: auto;
	margin-top: 6rem;
}
// Slider library //
.vueperslide {
	background-color: var(--news-bg);
	position: relative;
	background-repeat: no-repeat;
	background-size: auto;
	transition: background-color 0.3s ease-in-out;
	&::before {
		position: absolute;
		content: "";
		bottom: 0%;
		left: 0;
		width: 100%;
		height: 0.3rem;
		background: var(--danger);
	}
	&:hover {
		background-color: white;
		transition: background-color 0.3s ease-in-out;
		&::before {
			display: none;
		}
	}
	&__title {
		font-size: 2rem;
		text-transform: uppercase;
		position: absolute;
		bottom: -5%;
		color: var(--dark-blue);
		font-weight: bold;
		margin-bottom: 3rem;
	}
}
// Arrows //
.vueperslides__arrows {
	color: black;
}
.fa-chevron-left:before,
.fa-chevron-right:before {
	padding: 3rem;
	box-shadow: 5px 5px 15px 5px #cdcdcd;
	background: #fcf7f7;
}
// Bullets //
.vueperslides__bullet .default {
	background-color: transparent;
	border: 2px solid var(--dark-blue);
	box-shadow: none;
	transition: 0.3s;
	width: 1.2rem;
	height: 1.2rem;
}
.vueperslides__bullet--active .default {
	background-color: var(--dark-blue);
	transform: scale(0.7);
	&::before {
		content: "";
		position: absolute;
		top: -15px;
		right: -15px;
		bottom: -15px;
		left: -15px;
		border-radius: 50%;
		border: 3px solid #cfd8ea;
	}
}
.vueperslides__bullet span {
	display: block;
	color: #fff;
	font-size: 10px;
	opacity: 0.8;
}
.vueperslides__bullets {
	bottom: 5rem;
	@media only screen and (max-width: 900px) {
		bottom: 0rem;
	}
}

// HERO Carousel //

.hero {
	.vueperslide {
		background-size: cover;
		&::before {
			display: none;
		}
		// &__title {
		// 	text-align: left;
		// 	line-height: 15rem;
		// 	text-transform: none;
		// 	font-size: 17rem;
		// 	font-family: var(--hero-heading);
		// 	font-weight: 600;
		// 	color: white;
		// 	text-shadow: 4px 4px 2px rgba(150, 150, 150, 1);
		// 	top: 51%;
		// 	bottom: 0%;
		// 	transform: translateY(-50%);
		// 	left: 13%;
		// 	@media only screen and (max-width: 900px) {
		// 		font-size: 8rem;
		// 		line-height: 8rem;
		// 	}
		// 	@media only screen and (max-width: 360px) {
		// 		left: 7%;
		// 	}
		// }
		// &__content {
		// 	color: var(--dark-blue);
		// 	font-weight: bold;
		// 	font-size: 4.8rem;
		// 	position: absolute;
		// 	left: 14%;
		// 	top: 68%;
		// @media only screen and (max-width: 800px) {
		// 	font-size: 2.8rem;
		// }
		// }
		&__title {
			position: relative;
			text-align: left;
			line-height: 15rem;
			text-transform: none;
			font-size: 17rem;
			font-family: var(--hero-heading);
			font-weight: 600;
			color: white;
			text-shadow: 4px 4px 2px rgba(150, 150, 150, 1);
			margin-bottom: 0;
			bottom: 0%;
			@media only screen and (max-width: 900px) {
				font-size: 8rem;
				line-height: 8rem;
			}
		}
		&__content {
			color: var(--dark-blue);
			font-weight: bold;
			font-size: 4.8rem;
			@media only screen and (max-width: 800px) {
				font-size: 2.8rem;
			}
		}
	}
	.vueperslide__content-wrapper:not(.vueperslide__content-wrapper--outside-top):not(.vueperslide__content-wrapper--outside-bottom) {
		display: flex;
		align-items: flex-start;
		position: absolute;
		left: 25%;
		transform: translateX(-25%);
	}
}
</style>
