<template>
	<div class="about">
		<div class="about__info">
			<p class="home-about__info--quote" v-show="$route.name !== 'About'">
				“Ingunn Korsgård Hagen impressed the jury with a high professional level, clear vision and personality on stage,
				and is engaged as SSO’s assistant conductor for the 20/21 season!” <span>Stavanger Symphony Orchestra</span>
			</p>
			<p class="home-about__info--biography" v-show="$route.name !== 'About'">
				Ingunn Korsgård Hagen is a young, Norwegian conductor, experienced in wide variety of ensembles and repertoire.
				In the summer of 2020 she came all the way to the final of Talent Norway’s conducting competition where she won
				the job as assistent conductor for Stavanger Symphony Orchestra and a place in the prestigious elite program
				Dirigentforum for two years.
			</p>
			<div class="home-about__link" v-show="$route.name !== 'About'">
				<router-link :to="{ name: 'About' }">Biography</router-link>
			</div>
			<p class="about-page__info--bold" v-show="$route.name !== 'Home'">
				Ingunn Korsgård Hagen is a young, Norwegian conductor, experienced in wide variety of ensembles and repertoire.
				In the summer of 2020 she came all the way to the final of Talent Norway’s conducting competition where she won
				the job as assistent conductor for Stavanger Symphony Orchestra and a place in the prestigious elite program
				Dirigentforum for two years.
			</p>
			<p class="about-page__info--biography" v-show="$route.name !== 'Home'">
				She is currently studying her masters in conducting at the University in Stavanger with Bjarte Engeset, Peter
				Szilvay and Jukka Iisakkila as her professors. She has also completed her bachelors degree in conducting at the
				same university under professor Trond Korsgård.
			</p>
			<p class="about-page__info--biography" v-show="$route.name !== 'Home'">
				Hagen has participated in several masterclasses both in Norway and abroad with professors such as Ole Kristian
				Ruud, Sascha Goetzel, Christian Ehwald, James Gaffigan and Hannu Lintu. Through the masterclasses she has
				conducted ensembles such as Trondheim Symphony Orchestra, Stavanger Symphony Orchestra, Pazardzhik Symphony
				orchestra, Royal Norwegian Navy Band and Norwegian Armed Forces Band.
			</p>
			<p class="about-page__info--biography" v-show="$route.name !== 'Home'">
				From 2017 until 2019 she was a participant in Maestra, a talent program that focuses on young female conductors
				in Norway. As a part of the program she got to conduct and do concerts with several of the elite wind bands in
				Norway.
			</p>
			<p class="about-page__info--biography" v-show="$route.name !== 'Home'">
				In 2018 she started, together with Risto Sojakka, a professional Finnish-Norwegian chamber orchestra named
				Frostklang. The orchestra had their first concert in October 2018 in Pieksämäki, Finland.
			</p>
		</div>
		<div class="home-about__image">
			<img src="../../assets/ingunn-hagen-bio.jpg" alt="Picture of Ingunn" />
		</div>
	</div>
</template>

<script>
export default {};
</script>

<style scoped>
.about {
	background-color: #222328;
	color: white;
	margin: 0;
	display: flex;
	justify-content: center;
	align-items: center;
	flex-direction: column;
	text-align: left;
	padding-bottom: 50px;
}

@media screen and (min-width: 1024px) {
	.about {
		flex-direction: row-reverse;
		padding-top: 50px;
	}
}

.about__info {
	padding: 40px 20px;
	display: flex;
	justify-content: center;
	align-items: center;
	flex-direction: column;
	max-width: 500px;
}

.home-about__info--quote {
	font-style: italic;
	font-weight: 700;
	font-size: 20px;
	padding-bottom: 50px;
	color: #ffffffcc;
	line-height: 25px;
	letter-spacing: 1.3px;
}

.home-about__info--quote span {
	font-style: normal;
	font-weight: 500;
}

.home-about__info--biography {
	line-height: 25px;
	padding-bottom: 30px;
}

.home-about__link {
	width: 100%;
	display: flex;
	justify-content: center;
	align-items: center;
	padding-top: 20px;
}

.home-about__link a {
	cursor: pointer;
	text-transform: uppercase;
	border: 2px solid #5d72bf;
	border-radius: 10px;
	padding: 16px 40px;
	color: white;
	text-decoration: none;
	font-size: 14px;
	letter-spacing: 2px;
	transition: all 0.3s ease-in-out;
	background-color: transparent;
}

.home-about__link a:hover {
	background-color: #5d72bf;
}

.home-about__image {
	padding: 0 15px 50px 15px;
	display: flex;
	justify-content: center;
	align-items: center;
}

@media screen and (min-width: 1024px) {
	.home-about__image {
		padding: 40px 15px;
	}
}

.home-about__image img {
	width: 90%;
	max-width: 600px;
}

.about-page__info--bold {
	font-weight: 700;
	line-height: 25px;
	padding-bottom: 20px;
}

.about-page__info--biography {
	line-height: 25px;
	padding-bottom: 20px;
}
</style>
