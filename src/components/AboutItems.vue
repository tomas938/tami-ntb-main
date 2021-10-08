<template>
	<div class="about-items">
		<AboutItem
			v-for="(item, index) in aboutConent"
			:key="index"
			:img="item.img"
			:characteristic="item.characteristic"
			:textColor="item.textColor"
			:title="item.title"
			:description="item.description"
		>
			{{ item }}
		</AboutItem>
	</div>
</template>

<script>
import AboutItem from "../components/AboutItem.vue";
export default {
	props: ["aboutConent"],
	components: {
		AboutItem,
	},
};
</script>

<style lang="scss" scoped>
.about-items {
	display: grid;
	grid-template-columns: repeat(3, 1fr);
	grid-gap: 5rem;
	@media only screen and (max-width: 800px) {
		grid-template-columns: 1fr;
	}
}
</style>
