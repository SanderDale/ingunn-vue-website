<template>
	<div class="contact-info-container">
		<div class="contact-info">
			<h2>Contact Info</h2>
			<div>
				<h4>Email</h4>
				<p>post@ingunnhagen.com</p>
			</div>
			<div>
				<h4>Phone</h4>
				<p>+47 950 24 461</p>
			</div>
		</div>
		<div class="contact-image-container">
			<img src="../../assets/ingunn-park.jpg" alt="Ingunn in the park" />
		</div>
	</div>
</template>

<script>
export default {};
</script>

<style scoped>
.contact-info-container {
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
}

@media screen and (min-width: 658px) {
	.contact-info-container {
		flex-direction: row;
		padding: 80px 0;
	}
}

@media screen and (min-width: 1024px) {
	.contact-info-container {
		width: 100%;
		max-width: 900px;
	}
}

.contact-info {
	padding: 40px;
}

@media screen and (min-width: 1024px) {
	.contact-info {
		width: 450px;
		text-align: left;
	}
}

.contact-info h2 {
	font-size: 38px;
	font-weight: 400;
}

.contact-info div {
	padding-bottom: 10px;
	text-transform: lowercase;
}

.contact-info h4 {
	padding-top: 20px;
	font-size: 22px;
}

.contact-info p {
	padding-top: 10px;
	font-size: 20px;
	font-weight: 400;
}

@media screen and (min-width: 658px) {
	.contact-image-container {
		margin-right: 20px;
	}
}

.contact-image-container img {
	width: 100%;
	max-width: 80%;
	padding: 10px 0;
}

@media screen and (min-width: 1024px) {
	.contact-image-container img {
		max-width: 500px;
	}
}
</style>
