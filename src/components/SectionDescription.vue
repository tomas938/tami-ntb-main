<template>
	<div class="intro"><slot name="title"></slot></div>
	<h2><slot name="BigTitle"></slot></h2>
	<p v-if="$slots.description"><slot name="description"></slot></p>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.intro {
	font-size: 1.8rem;
	color: var(--light-blue);
	text-transform: uppercase;
	font-weight: 700;
	letter-spacing: 0.2rem;
}
h2 {
	margin-top: 1.5rem;
	margin-bottom: 3rem;
	font-size: 4.7rem;
	color: var(--dark-blue);
	@media only screen and (max-width: 600px) {
		font-size: 3.7rem;
	}
}
p {
	max-width: 90rem;
	font-size: 1.6rem;
	line-height: 2.5rem;
	margin: auto;
	color: var(--section-p-color);
	margin-bottom: 4.4rem;
}
</style>
