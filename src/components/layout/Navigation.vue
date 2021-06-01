<template>
	<nav>
		<ul>
			<li><router-link :to="{ name: 'Home' }">Home</router-link></li>
			<li><router-link :to="{ name: 'About' }">About</router-link></li>
			<li><router-link :to="{ name: 'Gallery' }">Gallery</router-link></li>
			<li><router-link :to="{ name: 'Contact' }">Contact</router-link></li>
		</ul>
	</nav>
</template>

<script>
export default {
	name: "Navigation",
};
</script>

<style>
nav {
	position: relative;
	z-index: 100;
	width: 100%;
	display: flex;
	justify-content: flex-end;
	align-items: center;
}

ul {
	display: flex;
	list-style: none;
	margin-right: 100px;
}

li {
	margin-right: 40px;
	font-size: 18px;
}

a {
	text-decoration: none;
	color: #d1d1d1;
}

a:hover {
	color: #ffffff;
}

a.router-link-exact-active {
	color: #ffffff;
}
</style>
