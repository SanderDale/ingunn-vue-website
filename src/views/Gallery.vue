<template>
	<Header title="Gallery" page="gallery" />
	<div class="gallery-background">
		<ImageGallery />
	</div>
</template>

<script>
import Header from "../components/layout/Header.vue";
import ImageGallery from "../components/content/ImageGallery.vue";

export default {
	name: "Gallery",
	components: {
		Header,
		ImageGallery,
	},
};
</script>

<style scoped>
.gallery-background {
	display: flex;
	justify-content: center;
	align-items: center;
	background-color: #222328;
}
</style>
