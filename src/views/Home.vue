<template>
	<div class="hero">
		<h1>Ingunn Korsgård Hagen</h1>
	</div>
	<AboutInfo />
	<HomeContact />
</template>

<script>
import AboutInfo from "../components/content/AboutInfo.vue";
import HomeContact from "../components/content/HomeContact.vue";

export default {
	name: "Home",
	components: {
		AboutInfo,
		HomeContact,
	},
	metaInfo: {
		title: "Home",
		titleTemplate: null,
	},
};
</script>

<style scoped>
.hero {
	width: 100%;
	height: 80vh;
	display: flex;
	justify-content: flex-start;
	align-items: flex-end;
	background-image: url(../assets/ingunn-hero.jpg);
	background-position: top center;
	background-size: cover;
}

@media screen and (min-width: 1024px) {
	.hero {
		height: 100vh;
		align-items: center;
	}
}

h1 {
	font-family: "Playfair Display SC", serif;
	font-weight: 400;
	padding-left: 30px;
	margin-bottom: 50px;
	max-width: 50px;
	font-size: 40px;
	color: #ffffff;
	letter-spacing: 4px;
	line-height: 140%;
	animation: slideInLeft 2s;
}

@keyframes slideInLeft {
	from {
		transform: translateX(-1000px);
	}
	to {
		transform: translateX(0);
	}
}

@media screen and (min-width: 481px) {
	h1 {
		font-size: 60px;
	}
}

@media screen and (min-width: 1024px) {
	h1 {
		font-size: 75px;
		padding-left: 100px;
	}
}
</style>
