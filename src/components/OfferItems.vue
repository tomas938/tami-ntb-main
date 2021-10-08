<template>
	<div class="offers">
		<OfferItem
			v-for="(offer, index) in offers"
			:key="index"
			:img="offer.img"
			:title="offer.title"
		>
			{{ offer }}
		</OfferItem>
	</div>
</template>

<script>
import OfferItem from "../components/OfferItem.vue";

export default {
	components: {
		OfferItem,
	},
	data() {
		return {
			offers: [
				{
					img: "offer-1",
					title: "základné informácie",
				},
				{
					img: "offer-2",
					title: "formuláre a tlačivá",
				},
				{
					img: "offer-3",
					title: "hlásenie o spotrebe mlieka",
				},
				{
					img: "offer-4",
					title: "mliečny automat",
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
.offers {
	display: grid;
	grid-template-columns: repeat(4, 1fr);
	gap: 2rem;
	@media only screen and (max-width: 800px) {
		grid-template-columns: repeat(2, 1fr);
		grid-gap: 4rem;
	}
	@media only screen and (max-width: 500px) {
		grid-template-columns: 1fr;
		grid-gap: 4rem;
	}
}
</style>
