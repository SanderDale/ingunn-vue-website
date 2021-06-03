<template>
	<Navigation />
	<router-view />
	<Footer />
</template>

<script>
import Navigation from "./components/layout/Navigation.vue";
import Footer from "./components/layout/Footer.vue";

export default {
	name: "App",
	components: {
		Navigation,
		Footer,
	},
};
</script>

<style>
* {
	margin: 0;
}

#app {
	position: relative;
	font-family: "Montserrat", sans-serif;
	font-weight: 500;
	text-align: center;
	color: #2c3e50;
	box-sizing: border-box;
	overflow: hidden;
}
</style>
