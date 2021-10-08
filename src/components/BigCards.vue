<template>
	<div class="cards">
		<BigCard
			v-for="(card, index) in data"
			:key="index"
			:heading="card.heading"
			:description="card.description"
			:img="card.img"
			:folder="card.folder"
		>
			{{ card }}
		</BigCard>
	</div>
</template>

<script>
import BigCard from "./BigCard.vue";
export default {
	components: {
		BigCard,
	},
	props: ["data"],
};
</script>

<style lang="scss" scoped>
.cards {
	margin-top: 6rem;
	position: relative;
	z-index: 2;
	margin-bottom: 7rem;
	display: grid;
	justify-items: center;
	grid-template-columns: repeat(3, 1fr);
	@media only screen and (max-width: 800px) {
		grid-template-columns: 1fr;
		grid-gap: 4rem;
	}
	grid-gap: 2rem;
}
</style>
