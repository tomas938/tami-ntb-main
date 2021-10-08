<template>
	<div class="about-item">
		<div class="rectangle">
			<img :src="require(`../assets/about/${img}.png`)" alt="" />
		</div>
		<span :class="textColor">{{ characteristic }}</span>
		<h2>{{ title }}</h2>
		<p>
			{{ description }}
		</p>
	</div>
</template>

<script>
export default {
	props: ["img", "characteristic", "title", "textColor", "description"],
};
</script>

<style lang="scss" scoped>
.about-item {
	display: flex;
	flex-direction: column;
	align-items: center;
	text-align: center;
	.rectangle {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 15rem;
		height: 15rem;
		margin-bottom: 6rem;
		background-color: white;
	}
	span {
		text-transform: uppercase;
		font-size: 1.8rem;
		font-weight: bold;
		color: green;
		margin-bottom: 2rem;
	}
	h2 {
		color: var(--dark-blue);
		font-size: 3.5rem;
		margin-bottom: 2.8rem;
	}
	p {
		font-size: 1.6rem;
		color: var(--section-p-color);
		max-width: 60rem;
	}
	.green {
		color: #48b01a;
	}
	.blue {
		color: #4da0d9;
	}
	.red {
		color: #e21e1c;
	}
}
</style>
