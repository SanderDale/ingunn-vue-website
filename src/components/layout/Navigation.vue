<template>
	<nav class="desktop-menu">
		<ul>
			<li><router-link :to="{ name: 'Home' }">Home</router-link></li>
			<li><router-link :to="{ name: 'About' }">About</router-link></li>
			<li><router-link :to="{ name: 'Gallery' }">Gallery</router-link></li>
			<li><router-link :to="{ name: 'Contact' }">Contact</router-link></li>
		</ul>
	</nav>
	<div class="menu-btn" :class="{ open: showMenu }" @click="toggleMenu">
		<div class="menu-btn__burger"></div>
	</div>
	<div class="mobile-menu" :class="{ open: showMenu }">
		<router-link :to="{ name: 'Home' }">Home</router-link>
		<router-link :to="{ name: 'About' }">About</router-link>
		<router-link :to="{ name: 'Gallery' }">Gallery</router-link>
		<router-link :to="{ name: 'Contact' }">Contact</router-link>
	</div>
</template>

<script>
export default {
	name: "Navigation",
	data() {
		return {
			showMenu: false,
		};
	},
	methods: {
		toggleMenu() {
			this.showMenu = !this.showMenu;
		},
	},
};
</script>

<style scoped>
.desktop-menu {
	position: absolute;
	right: 0;
	z-index: 100;
	width: 100%;
	display: flex;
	justify-content: flex-end;
	align-items: center;
	height: 130px;
}

@media screen and (max-width: 1024px) {
	.desktop-menu {
		display: none;
	}
}

ul {
	display: flex;
	list-style: none;
	margin-right: 5%;
}

li {
	padding: 0 30px;
	font-size: 25px;
}

a {
	text-decoration: none;
	color: #d1d1d1;
	transition: all 0.2s ease-in-out;
}

a:hover {
	color: #ffffff;
}

a.router-link-exact-active {
	color: #ffffff;
}

.menu-btn {
	position: absolute;
	right: 0;
	top: 0;
	display: flex;
	justify-content: center;
	align-items: center;
	width: 50px;
	height: 50px;
	cursor: pointer;
	transition: all 0.5s ease-in-out;
	z-index: 200;
	margin-left: auto;
	margin-right: 40px;
	margin-top: 20px;
}

@media screen and (min-width: 1024px) {
	.menu-btn {
		display: none;
	}
}

.menu-btn__burger {
	width: 30px;
	height: 3px;
	background: #fff;
	border-radius: 5px;
	box-shadow: 0 2px 5px rgba(255, 101, 47, 0.2);
	transition: all 0.5s ease-in-out;
	display: flex;
}

.menu-btn__burger::before,
.menu-btn__burger::after {
	content: "";
	position: absolute;
	width: 30px;
	height: 3px;
	background: #fff;
	border-radius: 5px;
	box-shadow: 0 2px 5px rgba(255, 101, 47, 0.2);
	transition: all 0.5s ease-in-out;
}

.menu-btn__burger::before {
	transform: translateY(-10px);
}

.menu-btn__burger::after {
	transform: translateY(10px);
}

.mobile-menu {
	position: absolute;
	transform: translateX(500px);
	overflow: hidden;
	opacity: 0;
	height: 0;
}

.mobile-menu.open {
	width: 100%;
	height: 100vh;
	z-index: 100;
	position: absolute;
	top: 0;
	right: 0;
	display: flex;
	flex-direction: column;
	justify-content: flex-start;
	align-items: center;
	background-color: rgb(27, 27, 27);
	padding-top: 100px;
	transition: all 0.5s ease-in-out;
	transform: translateX(0);
	overflow: hidden;
	opacity: 1;
}

@media screen and (min-width: 481px) {
	.mobile-menu.open {
		width: 50%;
	}
}

.mobile-menu a {
	margin-top: 40px;
	font-size: 25px;
}

/* ANIMATION */
.menu-btn.open .menu-btn__burger {
	transform: translateX(-50px);
	background: transparent;
	box-shadow: none;
}

.menu-btn.open .menu-btn__burger::before {
	transform: rotate(45deg) translate(35px, -35px);
}

.menu-btn.open .menu-btn__burger::after {
	transform: rotate(-45deg) translate(35px, 35px);
}
</style>
