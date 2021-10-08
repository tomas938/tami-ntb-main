<template>
	<router-view />
</template>

<style lang="scss">
@import url("https://fonts.cdnfonts.com/css/sofia-pro");
@import url("https://fonts.cdnfonts.com/css/myriad-pro");
//** */ Should be fixed i coudl't find victor script font for free :/ **//
@import url("https://fonts.googleapis.com/css2?family=Ephesis&display=swap");
//** */ Should be fixed i coudl't find victor script font for free :/ **//
* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}
a {
	text-decoration: none;
}
li {
	list-style: none;
}
:root {
	// Colors //
	--top-navigation-links: #5f6c8a;
	--top-navigation-bg: #f6f6fb;
	--top-navigation-detail: #e4e4ed;
	--dark-blue: #0e255b;
	--light-blue: #22479b;
	--footer-icon-bg: #f2f3f6;
	--news-bg: #f2f3f6;
	--news-p-color: #d6d6db;
	--danger: #e21c1a;
	--section-p-color: #afb5c2;
	--catalog-span: #aab8d9;
	--recipes-text-color: #9caed8;
	--mobile-hover-color: #add8e6;
	// Fonts //
	--sofia: "Sofia Pro", sans-serif;
	--myriad-pro: "Myriad Pro", sans-serif;
	//* CHANGE FONT FOR HERO HEADING *//
	--hero-heading: "Ephesis", cursive;
}

html {
	font-size: 62.5%;
	@media only screen and (max-width: 1300px) {
		font-size: 52.5%;
	}
	@media only screen and (max-width: 1100px) {
		font-size: 42.5%;
	}
}
body {
	font-size: 1.6rem;
	font-family: var(--sofia);
	overflow-x: hidden;
}
#app {
	overflow-x: hidden;
	-ms-scroll-chaining: none;
	overscroll-behavior: none;
	-webkit-perspective: 1px;
	perspective: 1px;
}
.noscroll {
	overflow: hidden;
}
.container {
	max-width: 1440px;
	margin: auto;
}
section {
	padding: 12.5rem;
	@media only screen and (max-width: 800px) {
		padding: 6.5rem 3rem;
	}
}
</style>
