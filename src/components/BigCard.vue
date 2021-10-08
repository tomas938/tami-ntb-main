<template>
	<router-link to="/" class="card">
		<img :src="require(`../assets/${folder}/${img}.png`)" alt="news" />
		<div class="card__content">
			<h3>{{ heading }}</h3>
			<p>
				{{ description }}
			</p>
			<router-link to="/">čítať viac</router-link>
		</div>
	</router-link>
</template>

<script>
export default {
	props: ["heading", "description", "img", "folder"],
};
</script>

<style lang="scss" scoped>
.card {
	display: flex;
	flex-direction: column;
	background-color: white;
	max-width: 50rem;
	transition: filter 0.3s ease-in-out;
	&:hover {
		filter: drop-shadow(8px 8px 10px rgba(219, 211, 211, 0.548)) invert(5%);
		transition: filter 0.3s ease-in-out;
	}
	img {
		width: 100%;
		object-fit: cover;
		position: relative;
	}
	&__content {
		padding: 4rem;
		position: relative;
		&::before {
			position: absolute;
			content: "";
			top: 0%;
			left: 0;
			width: 100%;
			height: 0.3rem;
			background: var(--danger);
		}
		h3 {
			font-size: 1.8rem;
			color: var(--dark-blue);
			margin-bottom: 2rem;
		}
		p {
			color: var(--news-p-color);
			margin-bottom: 4rem;
		}
		a {
			color: var(--danger);
		}
		h3,
		a {
			font-weight: bold;
			text-transform: uppercase;
		}
		p,
		a {
			font-size: 1.6rem;
		}
	}
}
</style>
