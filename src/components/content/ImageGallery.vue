<template>
	<div class="gallery-container" v-if="images.length">
		<div v-for="image in filteredImages" :key="image.id" class="gallery-image-container">
			<img :src="image.source_url" :alt="image.alt_text" class="gallery-image" />
		</div>
	</div>
	<div class="loading-container" v-else>
		<p class="loading">Loading...</p>
	</div>
</template>

<script>
export default {
	data() {
		return {
			images: [],
		};
	},
	mounted() {
		fetch("https://api.ingunnhagen.com/wp-json/wp/v2/media?per_page=20")
			.then((response) => response.json())
			.then((data) => (this.images = data))
			.catch((error) => console.log(error.message));
	},
	computed: {
		filteredImages() {
			return this.images.filter((image) => image.alt_text);
		},
	},
};
</script>

<style scoped>
.gallery-container {
	display: flex;
	flex-wrap: wrap;
	justify-content: center;
	align-items: center;
	width: 100%;
	max-width: 1600px;
	margin-top: 50px;
	margin-bottom: 50px;
	height: 100%;
	min-height: 70vh;
}

.gallery-image-container {
	padding: 15px;
}

.gallery-image {
	width: 100%;
	max-width: 300px;
	-webkit-box-shadow: 4px 4px 19px 2px rgba(0, 0, 0, 0.3);
	box-shadow: 4px 4px 19px 2px rgba(0, 0, 0, 0.3);
}

@media screen and (min-width: 481px) {
	.gallery-image {
		max-width: 500px;
	}
}

.loading-container {
	display: flex;
	justify-content: center;
	align-items: center;
	height: 70vh;
}

.loading {
	font-size: 40px;
	text-transform: uppercase;
	color: white;
}

@media screen and (min-width: 481px) {
	.loading {
		font-size: 60px;
	}
}

@media screen and (min-width: 1024px) {
	.loading {
		font-size: 80px;
	}
}
</style>
