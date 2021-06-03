<template>
	<div class="home-contact">
		<h3>Contact</h3>
		<p>+47 950 24 461</p>
		<p>post@ingunnhagen.com</p>
		<div class="home-contact__link">
			<router-link :to="{ name: 'Contact' }">Contact</router-link>
		</div>
	</div>
</template>

<script>
export default {};
</script>

<style scoped>
.home-contact {
	position: relative;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	height: 500px;
	color: white;
	background-color: black;
}

.home-contact::before {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	left: 0;
	bottom: 0;
	background-image: url(../../assets/home-contact-bg.jpg);
	background-position: center;
	background-repeat: no-repeat;
	background-size: cover;
	opacity: 0.6;
}

.home-contact h3 {
	position: relative;
	text-transform: uppercase;
	font-size: 26px;
	letter-spacing: 2.5px;
	padding-bottom: 35px;
}

.home-contact p {
	position: relative;
	line-height: 25px;
	padding-bottom: 15px;
}

.home-contact__link {
	position: relative;
	width: 100%;
	display: flex;
	justify-content: center;
	align-items: center;
	padding-top: 40px;
}

.home-contact__link a {
	cursor: pointer;
	text-transform: uppercase;
	border: 2px solid #ffffff;
	border-radius: 10px;
	padding: 16px 40px;
	color: #ffffff;
	text-decoration: none;
	font-size: 14px;
	letter-spacing: 2px;
	transition: all 0.3s ease-in-out;
	background-color: transparent;
}

.home-contact__link a:hover {
	background-color: #ffffff;
	color: #000000;
}
</style>
