<template>
	<header :class="{ about: page === 'about', gallery: page === 'gallery', contact: page === 'contact' }">
		<h1>{{ title }}</h1>
	</header>
</template>

<script>
export default {
	name: "Header",
	props: {
		title: String,
		page: String,
	},
};
</script>

<style scoped>
header {
	display: flex;
	justify-content: center;
	align-items: flex-end;
	position: relative;
	top: 0;
	left: 0;
	width: 100%;
	height: 230px;
	z-index: 10;
	background-color: black;
	color: #ffffff;
}

.about::before {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	left: 0;
	bottom: 0;
	background-image: url(../../assets/about-banner.jpg);
	background-position: center;
	background-repeat: no-repeat;
	background-size: cover;
	opacity: 0.5;
}

.gallery::before {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	left: 0;
	bottom: 0;
	background-image: url(../../assets/gallery-banner.jpg);
	background-position: center;
	background-repeat: no-repeat;
	background-size: cover;
	opacity: 0.5;
}

.contact::before {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	left: 0;
	bottom: 0;
	background-image: url(../../assets/contact-banner.jpg);
	background-position: center;
	background-repeat: no-repeat;
	background-size: cover;
	opacity: 0.5;
}

@media screen and (min-width: 1024px) {
	header {
		height: 330px;
	}
}

h1 {
	position: relative;
	font-size: 35px;
	font-weight: 400;
	padding-bottom: 60px;
}

@media screen and (min-width: 1024px) {
	h1 {
		font-size: 45px;
		padding-bottom: 100px;
	}
}
</style>
