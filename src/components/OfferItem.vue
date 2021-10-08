<template>
	<div class="offer">
		<div class="offer__img">
			<img :src="require(`../assets/Offers/${img}.png`)" alt="offer" />
		</div>
		<h3 class="offer__title">{{ title }}</h3>
	</div>
</template>

<script>
export default {
	props: ["img", "title"],
};
</script>

<style lang="scss" scoped>
.offer {
	&__img {
		position: relative;
		background-color: var(--news-bg);
		&::after {
			position: absolute;
			content: "";
			top: 125%;
			left: 0;
			width: 100%;
			height: 0.3rem;
			background: red;
		}
	}
	img {
		width: 14rem;
		height: 13rem;
	}
	&__title {
		text-transform: uppercase;
		font-size: 1.6rem;
		margin-top: 6rem;
		color: var(--dark-blue);
		font-weight: 800;
	}
}
</style>
