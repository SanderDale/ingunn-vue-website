<template>
	<header>
		<h1>{{ title }}</h1>
	</header>
</template>

<script>
export default {
	name: "Header",
	props: {
		title: String,
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
	background: slategray;
	color: #ffffff;
}

@media screen and (min-width: 1024px) {
	header {
		height: 330px;
	}
}

h1 {
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
