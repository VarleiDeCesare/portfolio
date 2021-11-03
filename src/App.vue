<template>
	<v-app id="inspire">
		<div>
			<v-app-bar color="accent-4" dark :style="`background-color: ${cor_header}`">
				<v-container>
					<v-row>
						<v-col class="d-flex justify-content-start">
							<v-app-bar-nav-icon @click.stop="drawer = !drawer" >
								<i class="fas fa-bars fa-lg"></i>
							</v-app-bar-nav-icon>
						</v-col>
						<v-col class="d-flex justify-content-end">
							<v-btn icon >
								<svg style="margin-right: 5px;" class="lampada" xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" height="24px" viewBox="0 0 24 24" width="24px" :fill="`${cor_letras}`">
									<rect fill="none" height="24" width="24"/>
									<path d="M12,7c-2.76,0-5,2.24-5,5s2.24,5,5,5s5-2.24,5-5S14.76,7,12,7L12,7z M2,13l2,0c0.55,0,1-0.45,1-1s-0.45-1-1-1l-2,0 c-0.55,0-1,0.45-1,1S1.45,13,2,13z M20,13l2,0c0.55,0,1-0.45,1-1s-0.45-1-1-1l-2,0c-0.55,0-1,0.45-1,1S19.45,13,20,13z M11,2v2 c0,0.55,0.45,1,1,1s1-0.45,1-1V2c0-0.55-0.45-1-1-1S11,1.45,11,2z M11,20v2c0,0.55,0.45,1,1,1s1-0.45,1-1v-2c0-0.55-0.45-1-1-1 C11.45,19,11,19.45,11,20z M5.99,4.58c-0.39-0.39-1.03-0.39-1.41,0c-0.39,0.39-0.39,1.03,0,1.41l1.06,1.06 c0.39,0.39,1.03,0.39,1.41,0s0.39-1.03,0-1.41L5.99,4.58z M18.36,16.95c-0.39-0.39-1.03-0.39-1.41,0c-0.39,0.39-0.39,1.03,0,1.41 l1.06,1.06c0.39,0.39,1.03,0.39,1.41,0c0.39-0.39,0.39-1.03,0-1.41L18.36,16.95z M19.42,5.99c0.39-0.39,0.39-1.03,0-1.41 c-0.39-0.39-1.03-0.39-1.41,0l-1.06,1.06c-0.39,0.39-0.39,1.03,0,1.41s1.03,0.39,1.41,0L19.42,5.99z M7.05,18.36 c0.39-0.39,0.39-1.03,0-1.41c-0.39-0.39-1.03-0.39-1.41,0l-1.06,1.06c-0.39,0.39-0.39,1.03,0,1.41s1.03,0.39,1.41,0L7.05,18.36z"/>
								</svg>
								<v-switch v-model="ex11" :color="`${cor_letras}`" hide-details></v-switch>
							</v-btn>
						</v-col>
					</v-row>
				</v-container>
			</v-app-bar>

			<v-navigation-drawer v-model="drawer" absolute right temporary>
				<v-list nav dense>
					<v-list-item-group v-model="group" active-class="deep-purple--text text--accent-4">
						<v-list-item to="/">
							<v-list-item-title>Home</v-list-item-title>
						</v-list-item>

						<v-list-item to="Portfolio">
							<v-list-item-title>Portfolio</v-list-item-title>
						</v-list-item>

						<v-list-item href="https://github.com/VarleiDeCesare/portfolio">
							<v-list-item-title>Código Fonte</v-list-item-title>
						</v-list-item>
					</v-list-item-group>
				</v-list>
			</v-navigation-drawer>
		</div>
		<!--		<v-app-bar app :color="`${cor_header}`" flat>-->
		<!--			<v-tabs centered center-active class="ml-n9" color="grey">-->
		<!--				<v-tab :to="{ name: 'Home', params: { cor_letras: cor_letras, }}" :style="`color: ${cor_letras}`">-->
		<!--					<i class="fas fa-home"></i>&nbsp;Home-->
		<!--				</v-tab>-->
		<!--				<v-tab :to="{ name: 'Portfolio', params: { cor_letras: cor_letras, cor: cor }}" :style="`color: ${cor_letras}`">-->
		<!--					<i class="fas fa-book"></i>&nbsp;Portfólio-->
		<!--				</v-tab>-->
		<!--				<v-tab @click="redireciona('https://github.com/VarleiDeCesare/portfolio')" :style="`color: ${cor_letras}`">-->
		<!--					<i class="fab fa-github"></i> &nbsp;Código Fonte-->
		<!--				</v-tab>-->
		<!--				<v-tab>-->
		<!--					<svg style="margin-right: 5px;" class="lampada" xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" height="24px" viewBox="0 0 24 24" width="24px" :fill="`${cor_letras}`">-->
		<!--						<rect fill="none" height="24" width="24"/>-->
		<!--						<path d="M12,7c-2.76,0-5,2.24-5,5s2.24,5,5,5s5-2.24,5-5S14.76,7,12,7L12,7z M2,13l2,0c0.55,0,1-0.45,1-1s-0.45-1-1-1l-2,0 c-0.55,0-1,0.45-1,1S1.45,13,2,13z M20,13l2,0c0.55,0,1-0.45,1-1s-0.45-1-1-1l-2,0c-0.55,0-1,0.45-1,1S19.45,13,20,13z M11,2v2 c0,0.55,0.45,1,1,1s1-0.45,1-1V2c0-0.55-0.45-1-1-1S11,1.45,11,2z M11,20v2c0,0.55,0.45,1,1,1s1-0.45,1-1v-2c0-0.55-0.45-1-1-1 C11.45,19,11,19.45,11,20z M5.99,4.58c-0.39-0.39-1.03-0.39-1.41,0c-0.39,0.39-0.39,1.03,0,1.41l1.06,1.06 c0.39,0.39,1.03,0.39,1.41,0s0.39-1.03,0-1.41L5.99,4.58z M18.36,16.95c-0.39-0.39-1.03-0.39-1.41,0c-0.39,0.39-0.39,1.03,0,1.41 l1.06,1.06c0.39,0.39,1.03,0.39,1.41,0c0.39-0.39,0.39-1.03,0-1.41L18.36,16.95z M19.42,5.99c0.39-0.39,0.39-1.03,0-1.41 c-0.39-0.39-1.03-0.39-1.41,0l-1.06,1.06c-0.39,0.39-0.39,1.03,0,1.41s1.03,0.39,1.41,0L19.42,5.99z M7.05,18.36 c0.39-0.39,0.39-1.03,0-1.41c-0.39-0.39-1.03-0.39-1.41,0l-1.06,1.06c-0.39,0.39-0.39,1.03,0,1.41s1.03,0.39,1.41,0L7.05,18.36z"/>-->
		<!--					</svg>-->
		<!--					<v-switch v-model="ex11" :color="`${cor_letras}`" hide-details></v-switch>-->
		<!--				</v-tab>-->
		<!--			</v-tabs>-->
		<!--		</v-app-bar>-->

		<v-main class="lighten-3" :style="`background-color: ${cor};`">
			<v-container>
				<v-row justify="center">
					<v-col cols="10" xl="5" lg="7">
						<v-sheet rounded="lg" :style="`background-color: ${cor}; color: ${cor_letras}`">
							<div class="container">
								<div class="row">
									<div class="col d-flex justify-content-center col-of-main-image">
										<img v-if="ex11" class="mr_robot_img" src="@/assets/mr_robot_white.png" alt="">
										<img v-if="!ex11" class="mr_robot_img" src="@/assets/mr_robot_black.png" alt="">
									</div>
								</div>
								<router-view></router-view>
							</div>
						</v-sheet>
					</v-col>
				</v-row>
			</v-container>
		</v-main>
		<v-footer padless :color="`${cor_header}`">
			<v-col class="text-center" cols="12">
				<h6 :style="`color: ${cor_letras}`">{{ new Date().getFullYear() }} — Varlei De Cesare</h6>
			</v-col>
		</v-footer>
	</v-app>
</template>
<script>
export default {
	data: () => ({
		ex11: true,
		cor_header: "#2b2b2f",
		cor: "#202023",
		cor_letras: "white",
		drawer: false,
		group: null,
	}),
	watch: {
		ex11() {
			if (this.ex11 === true) {
				this.cor_header = "#2b2b2f";
				this.cor = "#202023";
				this.cor_letras = "white"
			}
			if (this.ex11 === false) {
				this.cor_header = "#F4EDE4";
				this.cor = "#F0E7DB";
				this.cor_letras = "black"
			}
		},
		group () {
			this.drawer = false
		},
	},
	methods: {
		redireciona(link) {
			window.location.href = link;
		}
	},

}
</script>
<style scoped>
.v-application {
	font-family: 'Poppins', sans-serif;
}

:root {
	--azul-fraco: #4fd1c5;
}

a {
	text-decoration: none;
}

.col-of-main-image {
	margin-bottom: 25px;
}

.mr_robot_img {
	height: 230px;
}

</style>