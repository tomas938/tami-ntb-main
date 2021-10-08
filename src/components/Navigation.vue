<template>
	<div>
		<nav class="navigation">
			<div class="navigation__links">
				<ul class="left">
					<img
						id="logo-mobile"
						src="../assets/Home-page/logo.png"
						alt="tami-logo"
					/>

					<li>
						<router-link to="/">domov</router-link>
					</li>
					<li>
						<router-link to="/">aktuality</router-link>
					</li>
					<li>
						<router-link to="/">recepty</router-link>
					</li>
					<li>
						<router-link class="last" to="/">školské mlieko</router-link>
					</li>
				</ul>
				<ul class="right">
					<li>
						<router-link to="/">súťaž</router-link>
					</li>
					<li>
						<router-link to="/">projekty</router-link>
					</li>
					<li>
						<router-link to="/">reality</router-link>
					</li>
					<li>
						<router-link to="/">kariéra</router-link>
					</li>
					<li>
						<router-link class="last" to="/">kontaktujte nás</router-link>
					</li>
					<div class="lang">
						<img src="../assets/Home-page/worldwide.png" alt="world" />
						<span>SK</span>
					</div>
					<div class="hamburger" @click="toggleMobileNav" v-show="mobile">
						<span class="line" :class="{ mobile: mobileNav }"></span>
						<span class="line" :class="{ mobile: mobileNav }"></span>
						<span class="line" :class="{ mobile: mobileNav }"></span>
					</div>
					<div>
						<ul
							class="mobile__links"
							:class="{ mobile: mobileNav }"
							v-show="mobileNav"
						>
							<li>
								<router-link class="link" :to="{ name: 'Home' }"
									>Domov</router-link
								>
							</li>
							<li>
								<router-link class="link" :to="{ name: 'Home' }"
									>aktuality</router-link
								>
							</li>
							<li>
								<router-link class="link" :to="{ name: 'Home' }"
									>recepty</router-link
								>
							</li>
							<li>
								<router-link class="link" :to="{ name: 'Home' }"
									>školské mlieko</router-link
								>
							</li>
							<li>
								<router-link class="link" :to="{ name: 'Home' }"
									>súťaž</router-link
								>
							</li>
							<li>
								<router-link class="link" :to="{ name: 'Home' }"
									>projekty</router-link
								>
							</li>
							<li>
								<router-link class="link" :to="{ name: 'Home' }"
									>reality</router-link
								>
							</li>
							<li>
								<router-link class="link" :to="{ name: 'Home' }"
									>kariéra</router-link
								>
							</li>
						</ul>
					</div>
				</ul>
			</div>
			<div class="navigation__menu">
				<ExpandButton
					@click="toggleProducts"
					:class="{ active: expandProducts }"
					>Naše produkty</ExpandButton
				>
				<img id="logo" src="../assets/Home-page/logo.png" alt="tami-logo" />
				<div class="about">
					<img src="../assets/Home-page/eu.png" alt="europe union" />
					<img src="../assets/Home-page/flower.png" alt="flower" />
					<div class="eshop">
						<svg
							height="512pt"
							viewBox="0 -31 512.00026 512"
							width="512pt"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="m164.960938 300.003906h.023437c.019531 0 .039063-.003906.058594-.003906h271.957031c6.695312 0 12.582031-4.441406 14.421875-10.878906l60-210c1.292969-4.527344.386719-9.394532-2.445313-13.152344-2.835937-3.757812-7.269531-5.96875-11.976562-5.96875h-366.632812l-10.722657-48.253906c-1.527343-6.863282-7.613281-11.746094-14.644531-11.746094h-90c-8.285156 0-15 6.714844-15 15s6.714844 15 15 15h77.96875c1.898438 8.550781 51.3125 230.917969 54.15625 243.710938-15.941406 6.929687-27.125 22.824218-27.125 41.289062 0 24.8125 20.1875 45 45 45h272c8.285156 0 15-6.714844 15-15s-6.714844-15-15-15h-272c-8.269531 0-15-6.730469-15-15 0-8.257812 6.707031-14.976562 14.960938-14.996094zm312.152343-210.003906-51.429687 180h-248.652344l-40-180zm0 0"
							/>
							<path
								d="m150 405c0 24.8125 20.1875 45 45 45s45-20.1875 45-45-20.1875-45-45-45-45 20.1875-45 45zm45-15c8.269531 0 15 6.730469 15 15s-6.730469 15-15 15-15-6.730469-15-15 6.730469-15 15-15zm0 0"
							/>
							<path
								d="m362 405c0 24.8125 20.1875 45 45 45s45-20.1875 45-45-20.1875-45-45-45-45 20.1875-45 45zm45-15c8.269531 0 15 6.730469 15 15s-6.730469 15-15 15-15-6.730469-15-15 6.730469-15 15-15zm0 0"
							/>
						</svg>
						<router-link to="/">E-SHOP</router-link>
					</div>
				</div>
				<div class="navigation__expand" :class="{ active: expandProducts }">
					<ExpandProducts></ExpandProducts>
				</div>
			</div>
		</nav>
	</div>
</template>

<script>
import ExpandButton from "./ExpandButton.vue";
import ExpandProducts from "./ExpandProducts.vue";
export default {
	components: {
		ExpandButton,
		ExpandProducts,
	},
	data() {
		return {
			expandProducts: false,
			body: null,
			mobile: null,
			mobileNav: null,
			windowWidth: null,
		};
	},
	created() {
		window.addEventListener("resize", this.checkScreenSize);
		this.checkScreenSize();
		this.body = document.querySelector("body");
	},
	methods: {
		toggleProducts() {
			this.expandProducts = !this.expandProducts;
		},
		toggleMobileNav() {
			this.mobileNav = !this.mobileNav;
			this.body.classList.toggle("noscroll");
		},
		checkScreenSize() {
			this.windowWidth = window.innerWidth;
			if (this.windowWidth <= 900) {
				this.mobile = true;
				return;
			}
			this.mobile = false;
			this.mobileNav = false;
			return;
		},
	},
};
</script>

<style lang="scss" scoped>
.navigation {
	width: 100%;
	font-family: var(--sofia);
	font-size: 1.5rem;
	&__links {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 3rem;
		background-color: var(--top-navigation-bg);
		@media only screen and (max-width: 900px) {
			a {
				display: none;
			}
		}
		.left,
		.right {
			display: flex;
			gap: 5rem;
			@media only screen and (max-width: 900px) {
				gap: 0rem;
			}
		}

		a {
			font-weight: bold;
			position: relative;
			text-transform: uppercase;
			color: var(--top-navigation-links);
		}
		a:nth-child(1) {
			margin-left: 0;
		}
		a::after {
			position: absolute;
			pointer-events: none;
			content: "";
			top: 50%;
			right: -2.5rem;
			transform: translateY(-50%);
			width: 0.1rem;
			height: 3rem;
			background-color: #e4e4ed;
		}
		a:hover {
			color: var(--light-blue);
			transition: color 0.3s ease-in-out;
		}
		.right {
			display: flex;
			align-items: center;
		}
		// THIS SHOULD BE FIXED !!!  LAST:CHILD NOT WORKING !!!//
		.last::after {
			display: none;
		}
		// THIS SHOULD BE FIXED !!! //
	}
	&__menu {
		position: relative;
		display: flex;
		justify-content: space-between;
		background-color: white;
		padding: 1rem;
		@media only screen and (max-width: 900px) {
			// padding: 1rem 0rem;
			display: none;
		}
		#logo {
			position: absolute;
			z-index: 2;
			left: 50%;
			top: -28%;
			width: 18.9rem;
			transform: translateX(-50%);
			@media only screen and (max-width: 900px) {
				display: none;
			}
		}
		.about {
			display: flex;
			align-items: center;
			gap: 2.5rem;
			background-color: white;
			img {
				@media only screen and (max-width: 900px) {
					display: none;
				}
			}
		}
		.eshop {
			display: flex;
			align-items: center;
			gap: 1rem;
			padding: 1rem 3rem;
			background: var(--dark-blue);
			cursor: pointer;
			&:hover {
				background-color: var(--light-blue);
				transition: background-color 0.2s ease-in-out;
			}
			a {
				color: white;
				font-weight: bold;
				font-size: 1.3rem;
				letter-spacing: 0.2rem;
			}
		}
		svg {
			width: 3rem;
			height: 3rem;
			fill: #8792ad;
		}
	}
	&__expand {
		position: absolute;
		z-index: 10;
		pointer-events: none;
		opacity: 0;
		top: 50%;
		left: 0;
		width: 100%;
		background-color: white;
		transition: all 0.3s ease-in-out;
	}
	.active {
		top: 100%;
		opacity: 1;
		transition: all 0.3s ease-in-out;
	}
}
.hamburger {
	cursor: pointer;
	z-index: 5;
	.line {
		display: block;
		width: 2.8rem;
		height: 0.4rem;
		margin: 0.5rem auto;
		background-color: var(--dark-blue);
		transition: 0.25s ease-in-out;
	}
	.mobile {
		background-color: white;
		&:nth-child(1) {
			transform: translateY(0.5rem) rotate(45deg);
		}
		&:nth-child(2) {
			opacity: 0;
		}
		&:nth-child(3) {
			transform: translateY(-1.3rem) rotate(-45deg);
		}
	}
}
.mobile__links {
	position: absolute;
	top: 0;
	left: 0;
	width: 100vw;
	height: 150vh;
	padding-top: 15rem;
	background-color: var(--light-blue);
	z-index: 4;
	display: block !important;
	clip-path: circle(0% at 100% 0);
	opacity: 0;
	transition: clip-path 0.5s ease-in-out, 0s opacity 1s;
	li {
		margin-bottom: 4rem;
		text-align: center;
	}
	a {
		display: block;
		color: white;
		font-size: 1.8rem;
		&:hover {
			color: var(--mobile-hover-color);
		}
	}
}

#logo-mobile {
	display: none;
	@media only screen and (max-width: 900px) {
		display: block;
		position: absolute;
		top: 1rem;
		height: 10rem;
		width: 13.3rem;
	}
}
.mobile {
	clip-path: circle(141.6% at 100% 0);
	opacity: 1;
	transition: clip-path 0.5s linear;
}
.lang {
	display: flex;
	align-items: center;
	gap: 1rem;
	span {
		color: #37374f;
		font-weight: bold;
	}
	img {
		width: 2rem;
		height: 2rem;
	}
	@media only screen and (max-width: 900px) {
		display: none;
	}
}
</style>
