<template>
	<Header title="About" page="about" />
	<AboutInfo />
</template>

<script>
import Header from "../components/layout/Header.vue";
import AboutInfo from "../components/content/AboutInfo.vue";

export default {
	name: "Home",
	components: {
		Header,
		AboutInfo,
	},
};
</script>
