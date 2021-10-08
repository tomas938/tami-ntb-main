<template>
	<div class="expand">
		<img src="../assets/Home-page/awesome.png" alt="" />
		<span><slot></slot></span>
		<svg
			version="1.1"
			id="Capa_1"
			fill="white"
			xmlns="http://www.w3.org/2000/svg"
			xmlns:xlink="http://www.w3.org/1999/xlink"
			x="0px"
			y="0px"
			width="451.847px"
			height="451.847px"
			viewBox="0 0 451.847 451.847"
			style="enable-background:new 0 0 451.847 451.847;"
			xml:space="preserve"
		>
			<g>
				<path
					d="M225.923,354.706c-8.098,0-16.195-3.092-22.369-9.263L9.27,151.157c-12.359-12.359-12.359-32.397,0-44.751
		c12.354-12.354,32.388-12.354,44.748,0l171.905,171.915l171.906-171.909c12.359-12.354,32.391-12.354,44.744,0
		c12.365,12.354,12.365,32.392,0,44.751L248.292,345.449C242.115,351.621,234.018,354.706,225.923,354.706z"
				/>
			</g>
			<g></g>
			<g></g>
			<g></g>
			<g></g>
			<g></g>
			<g></g>
			<g></g>
			<g></g>
			<g></g>
			<g></g>
			<g></g>
			<g></g>
			<g></g>
			<g></g>
			<g></g>
		</svg>
	</div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.expand {
	background-color: #22479b;
	max-width: 31rem;
	padding: 1rem 3rem;
	display: flex;
	align-items: center;
	gap: 1.3rem;
	cursor: pointer;
	transition: 0.2s background-color ease-in-out;
	font-family: var(--sofia);
	&:hover {
		background-color: rgb(9, 41, 90);
		transition: 0.2s background-color ease-in-out;
	}
}
span {
	color: white;
	text-transform: uppercase;
	font-size: 1.6rem;
}
img {
	width: 1.5rem;
	height: 1.5rem;
}
svg {
	width: 1rem;
	height: 1rem;
	margin-left: 4.5rem;
}
.active {
	background-color: var(--danger);
}
</style>
