<template>
	<Header title="Contact" page="contact" />
	<div class="contact-background">
		<ContactInfo />
	</div>
</template>

<script>
import Header from "../components/layout/Header.vue";
import ContactInfo from "../components/content/ContactInfo.vue";

export default {
	name: "Contact",
	components: {
		Header,
		ContactInfo,
	},
};
</script>

<style scoped>
.contact-background {
	display: flex;
	justify-content: center;
	align-items: center;
	background-color: #222328;
	color: white;
}
</style>
