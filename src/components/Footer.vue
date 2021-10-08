<template>
	<footer>
		<div class="container">
			<div class="adress">
				<img src="../assets/Home-page/logo.png" alt="logo" />
				<span>tatranská mliekáreň a.s</span>
				<span>nad traťou 26</span>
				<span>060 01 Kežmarok</span>
				<div class="socials">
					<router-link to="/"
						><svg
							aria-hidden="true"
							focusable="false"
							data-prefix="fab"
							data-icon="facebook-f"
							class="svg-inline--fa fa-facebook-f fa-w-10"
							role="img"
							xmlns="http://www.w3.org/2000/svg"
							viewBox="0 0 320 512"
						>
							<path
								fill="#3c68cd"
								d="M279.14 288l14.22-92.66h-88.91v-60.13c0-25.35 12.42-50.06 52.24-50.06h40.42V6.26S260.43 0 225.36 0c-73.22 0-121.08 44.38-121.08 124.72v70.62H22.89V288h81.39v224h100.17V288z"
							></path>
						</svg>
					</router-link>

					<router-link to="/"
						><svg
							aria-hidden="true"
							focusable="false"
							data-prefix="fab"
							data-icon="instagram"
							class="svg-inline--fa fa-instagram fa-w-14"
							role="img"
							xmlns="http://www.w3.org/2000/svg"
							viewBox="0 0 448 512"
						>
							<path
								fill="#cd6c3c"
								d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z"
							></path></svg
					></router-link>
					<router-link to="/"
						><svg
							aria-hidden="true"
							focusable="false"
							data-prefix="fab"
							data-icon="youtube"
							class="svg-inline--fa fa-youtube fa-w-18"
							role="img"
							xmlns="http://www.w3.org/2000/svg"
							viewBox="0 0 576 512"
						>
							<path
								fill="#e21e1c"
								d="M549.655 124.083c-6.281-23.65-24.787-42.276-48.284-48.597C458.781 64 288 64 288 64S117.22 64 74.629 75.486c-23.497 6.322-42.003 24.947-48.284 48.597-11.412 42.867-11.412 132.305-11.412 132.305s0 89.438 11.412 132.305c6.281 23.65 24.787 41.5 48.284 47.821C117.22 448 288 448 288 448s170.78 0 213.371-11.486c23.497-6.321 42.003-24.171 48.284-47.821 11.412-42.867 11.412-132.305 11.412-132.305s0-89.438-11.412-132.305zm-317.51 213.508V175.185l142.739 81.205-142.739 81.201z"
							></path></svg
					></router-link>
				</div>
			</div>
			<div class="products">
				<h3>Naše produkty</h3>
				<div class="links">
					<div class="left">
						<router-link to="/">mlieko</router-link>
						<router-link to="/">smotana</router-link>
						<router-link to="/">kyslomliečne výrobky</router-link>
						<router-link to="/">syry</router-link>
						<router-link to="/">nátierky</router-link>
						<router-link to="/">maslo/brynzda</router-link>
						<router-link to="/">tvaroh/riccota</router-link>
					</div>
					<div class="right">
						<router-link to="/">dezerty</router-link>
						<router-link to="/">jogurty</router-link>
						<router-link to="/">gastro výrobky</router-link>
						<router-link to="/">bio výrobky</router-link>
						<router-link to="/">bezlaktózové výrobky</router-link>
						<router-link to="/">špeciálne produkty</router-link>
					</div>
				</div>
			</div>
			<div class="navigation">
				<h3>Navigácia</h3>
				<div class="links">
					<router-link to="/">domov</router-link>
					<router-link to="/">školské mlieko</router-link>
					<router-link to="/">aktuality</router-link>
					<router-link to="/">projekty</router-link>
					<router-link to="/">sútaž</router-link>
					<router-link to="/">recepty</router-link>
					<router-link to="/">o nás</router-link>
					<router-link to="/">kariéra</router-link>
					<router-link to="/">kontakt</router-link>
				</div>
			</div>
		</div>
		<div class="rights">
			<p>
				Všetky práva vyhradené &copy; 2021 Vytvorené agentúrou
				<router-link to="https://www.invelity.com/" target="_blank">
					<svg
						version="1.1"
						xmlns="http://www.w3.org/2000/svg"
						x="0px"
						y="0px"
						viewBox="0 0 162 23"
						xml:space="preserve"
					>
						<path d="M0,23h6.7V0H0V23z" />
						<path d="M9.9,23h6.7V10.9L25.1,23h5.7V0h-6.7v12.2L15.5,0H9.9V23z" />
						<path d="M42.1,23h7.1l8.8-23h-7l-5.3,15.2L40.2,0h-7L42.1,23z" />
						<path
							d="M60.4,23h17.3v-5.1H67v-3.8h9.3V8.9H67V5.1h10.6V0H60.4V23z"
						/>
						<path d="M79.8,23h17v-5.1H86.5V0h-6.7V23z" />
						<path d="M125.1,23h6.7V5h6.4V0h-19.5v5h6.4V23z" />
						<path
							d="M147.1,23h6.7v-8.4L162,0h-7l-4.6,8.7L145.8,0h-7l8.2,14.6V23z"
						/>
						<path class="highlight" d="M97.7,23h6.8l13.2-22.9h-6.8L97.7,23z" />
					</svg>
				</router-link>
			</p>
		</div>
	</footer>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.container {
	margin-top: 11rem;
	padding-bottom: 14rem;
	display: grid;
	grid-template-columns: 1fr 2fr 1fr;
	grid-gap: 16rem;
	@media only screen and (max-width: 1350px) {
		grid-gap: 10rem;
	}
	@media only screen and (max-width: 700px) {
		margin-top: 6.5rem;
		grid-template-columns: 1fr;
		justify-items: center;
		grid-gap: 7rem;
		.navigation {
			width: 20rem;
		}
		.products {
			width: 20rem;
		}
	}
	.adress {
		display: flex;
		flex-direction: column;
		img {
			width: 18rem;
		}
		span,
		.socials {
			display: flex;
			gap: 1rem;
			margin-left: 2.5rem;
			@media only screen and (max-width: 700px) {
				margin-left: 0;
			}
		}
		.socials a {
			padding: 1rem;
			background-color: var(--footer-icon-bg);
			transition: background-color 0.3s ease-in-out;
			&:hover {
				background-color: rgb(242, 255, 56);
				transition: background-color 0.3s ease-in-out;
			}
		}
		.socials svg {
			height: 1.8rem;
			width: 2rem;
		}
	}
	.products {
		.links {
			display: flex;
			gap: 16rem;
			@media only screen and (max-width: 700px) {
				flex-direction: column;
				gap: 2rem;
			}
		}
		.left,
		.right {
			display: flex;
			flex-direction: column;
			gap: 2rem;
		}
	}
	.navigation {
		.links {
			display: flex;
			flex-direction: column;
			gap: 2rem;
		}
	}
}
.rights {
	border-top: 1px solid var(--footer-icon-bg);
	padding: 5rem 3rem 25rem 3rem;
	grid-column: 2/3;
	p {
		width: 100%;
		text-align: center;
		color: var(--section-p-color);
	}
	svg {
		cursor: pointer;
		margin-left: 0.5rem;
		height: 1.5rem;
		width: 10rem;
		fill: #404a74;
		transition: fill 0.5s;
		@media only screen and (max-width: 400px) {
			margin-top: 0.5rem;
		}
		&:hover {
			transition: fill 0.5s;
			fill: #e84948;
			.highlight {
				transition: fill 0.25s;
				fill: #404a74;
			}
		}
	}
	.highlight {
		transition: fill 0.25s;
		fill: #e84948;
	}
}
h3 {
	color: var(--light-blue);
	font-size: 1.8rem;
	margin-bottom: 5rem;
}
a,
span {
	text-transform: uppercase;
	font-size: 1.4rem;
	color: var(--recipes-text-color);
	font-weight: bold;
}
span {
	letter-spacing: 0.1rem;
	margin-bottom: 1.9rem;
}
a:hover {
	color: var(--light-blue);
	transition: color 0.3s ease-in-out;
}
</style>
