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
	border: 1px solid black;
	display: flex;
	justify-content: space-evenly;
	align-items: center;
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 200px;
	z-index: 10;
	background: slategray;
	color: #ffffff;
}

h1 {
	font-size: 35px;
	font-weight: 400;
}
</style>
