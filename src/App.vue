<template>
	<Navigation />
	<router-view />
</template>

<script>
import Navigation from "./components/layout/Navigation.vue";

export default {
	name: "App",
	components: {
		Navigation,
	},
};
</script>

<style>
#app {
	font-family: "Montserrat", sans-serif;
	font-weight: 500;
	text-align: center;
	color: #2c3e50;
}
</style>
