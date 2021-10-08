<template>
	<div class="products">
		<ExpandProduct
			v-for="(product, index) in products"
			:key="index"
			:title="product.title"
			:img="product.img"
		>
			{{ product }}
		</ExpandProduct>
	</div>
</template>

<script>
import ExpandProduct from "./ExpandProduct";
export default {
	components: {
		ExpandProduct,
	},
	data() {
		return {
			products: [
				{
					img: "milk",
					title: "mlieko",
				},
				{
					img: "cream",
					title: "smotana",
				},
				{
					img: "milk-products",
					title: "kyslomliečne výrobky",
				},
				{
					img: "cheese",
					title: "syry",
				},
				{
					img: "spread",
					title: "nátierky",
				},
				{
					img: "butter",
					title: "maslo a bryndza",
				},
				{
					img: "deserts",
					title: "dezerty",
				},
				{
					img: "yoghurts",
					title: "jogurty",
				},
				{
					img: "gastro",
					title: "gastro",
				},
				{
					img: "bio",
					title: "bio výrobky",
				},
				{
					img: "no-lactose",
					title: "bezlkatózové výrobky",
				},
				{
					img: "cottage",
					title: "tvaroh a riccota",
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
.products {
	display: grid;
	grid-template-columns: repeat(auto-fit, 21rem);
	justify-content: center;
	box-shadow: 5px 50px 50px 15px rgba(0, 0, 0, 0.64);
}
</style>
