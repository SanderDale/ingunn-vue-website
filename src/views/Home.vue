<template>
	<div class="home">
		<div class="hero">
			<h1>Ingunn Korsgård Hagen</h1>
		</div>
	</div>
</template>

<script>
export default {
	name: "Home",
};
</script>

<style scoped>
.hero {
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 100vh;
	display: flex;
	justify-content: flex-start;
	align-items: center;
	background: slategray;
}

h1 {
	font-family: "Playfair Display SC", serif;
	padding-left: 100px;
	max-width: 50px;
	font-size: 60px;
	color: #ffffff;
}
</style>
