<template>
	<div class="product">
		<img
			:src="require(`../assets/navigation-products/${img}.png`)"
			:alt="title"
		/>
		<h4>{{ title }}</h4>
	</div>
</template>

<script>
export default {
	props: ["img", "title"],
};
</script>

<style lang="scss" scoped>
.product {
	position: relative;
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	padding: 3rem;
	text-align: center;
	gap: 3rem;
	&::after {
		position: absolute;
		pointer-events: none;
		content: "";
		top: 50%;
		right: -0.5rem;
		transform: translateY(-50%);
		width: 0.1rem;
		height: 15rem;
		background-color: #e4e4ed;
	}
}
h4 {
	color: var(--dark-blue);
	font-size: 1.4rem;
	font-weight: bold;
	text-transform: uppercase;
}
</style>
