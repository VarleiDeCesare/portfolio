<template>
	<div>
		<v-container>
			<v-row justify="center" style="margin-top: 20px">
				<h6>Projetos</h6>
			</v-row>
			<v-row justify="center">
				<!--fixme Para cada novo post, duplique uma dessas colunas, troque os dados, troque a variavel dialog e declare a mesma no data()-->

				<!--Painel Ejetar-->
				<v-col cols="10" sm="5" lg="5" class="project-item">
					<v-card>
						<v-img src="../assets/painel.png" max-height="125" contain></v-img>
						<v-card-title class="text-h6">
							<v-dialog class="dialog-here" v-model="dialog" fullscreen hide-overlay transition="dialog-bottom-transition">
								<template v-slot:activator="{ on, attrs }">
									<div class="data-project">
										<h5 class="title-project hvr-pop" v-bind="attrs" v-on="on">Painel Ejetar</h5>
										<p class="text-project">Painel para monitorar consumo de Banda e Disco Rígido de clientes do servidor, integração com pagamento</p>
									</div>

								</template>
								<div class="content-post-project-father">
									<v-toolbar dark color="#e59447">
										<v-btn icon dark @click="dialog = false">
											<v-icon>mdi-close</v-icon>
										</v-btn>
									</v-toolbar>
									<v-container>
										<v-row justify="center">
											<v-col cols="12" lg="7">
												<div class="d-flex justify-content-around content-post-project">
													<div>
														<h4>Painel Grupo Ejetar</h4>
														<div class="ml-2">
															<h6 class="d-flex">
																<i class="fas fa-laptop"></i>&nbsp;Windows/MacOS/Linux/iOS/Android
															</h6>
															<h6 class="d-flex">
																<i class="far fa-keyboard"></i>&nbsp;Laravel, Vue.js, PHP
															</h6>
															<h6 class="d-flex">
																<i class="fas fa-external-link-alt"></i>&nbsp;painel.grupoejetar.com.br
															</h6>
														</div>
													</div>
													<div class="about-project">
														<p>O Painel tem o propósito de captar consumos de Disco e de Banda Larga de cada cliente, fazer o cálculo levando em consideração os gastos e lançar uma cobrança na Stripe. Stripe é a integração na qual a Stack Laravel Cashier lança a cobrança e envia e-mail com o boleto para o cliente poder fazer o pagamento</p>
													</div>
												</div>
											</v-col>
										</v-row>
										<v-row justify="center" class="images-project">
											<v-col class="d-flex child-flex" cols="12" lg="6">
												<v-img src="../assets/project_painel.png" aspect-ratio="1" class="lighten-2" contain>
													<template v-slot:placeholder>
														<v-row class="fill-height ma-0" align="center" justify="center">
															<v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
														</v-row>
													</template>
												</v-img>
											</v-col>
											<v-col class="d-flex child-flex" cols="12" lg="6">
												<v-img src="../assets/project_painel2.png" class="lighten-2" contain>
													<template v-slot:placeholder>
														<v-row align="center" justify="center">
															<v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
														</v-row>
													</template>
												</v-img>
											</v-col>
										</v-row>
										<v-row>
											<small class="text-center data-oculted">*Dados ocultados para proteção de dados internos*</small>
										</v-row>
									</v-container>
								</div>
							</v-dialog>
						</v-card-title>
					</v-card>
				</v-col>

				<!--CFR Agrotehc-->
				<v-col cols="10" sm="5" lg="5" class="project-item">
					<v-card>
						<v-img src="../assets/project_agrotehc.png" max-height="125" contain></v-img>
						<v-card-title class="text-h6">
							<v-dialog class="dialog-here" v-model="dialog1" fullscreen hide-overlay transition="dialog-bottom-transition">
								<template v-slot:activator="{ on, attrs }">
									<div class="data-project">
										<h5 class="title-project hvr-pop" v-bind="attrs" v-on="on">CFR Agrotech</h5>
										<p class="text-project">Aplicativo para controle de finanças Rurais (em desenvolvimento)</p>
									</div>
								</template>
								<div class="content-post-project-father">
									<v-toolbar dark color="#e59447">
										<v-btn icon dark @click="dialog1 = false">
											<v-icon>mdi-close</v-icon>
										</v-btn>
									</v-toolbar>
									<v-container>
										<v-row justify="center">
											<v-col cols="12" lg="7">

												<div class="d-flex justify-content-around content-post-project">
													<div>
														<h4>Controle de Finanças Agrícolas</h4>
														<div class="ml-2">
															<h6 class="d-flex">
																<i class="fas fa-laptop"></i>&nbsp;Windows/MacOS/Linux/iOS/Android
															</h6>
															<h6 class="d-flex">
																<i class="far fa-keyboard"></i>&nbsp;Laravel, Vue.js, PHP
															</h6>
															<h6 class="d-flex">
																<i class="fas fa-external-link-alt"></i>&nbsp;localhost
															</h6>
														</div>
													</div>
													<div class="about-project">
														<p>O aplicativo tem como propósito dar possiblidade para que produtores rurais possam cadastrar dados em suas safras de cada lavoura, para que possa ter um conhecimento maior sobre gastos, e ganhos em um único histórico, simples e funcional. O projeto ainda está em desenvolvimento e tem como ideia central o aprendizado do desenvolvedor.</p>
													</div>
												</div>
											</v-col>
										</v-row>
										<v-row justify="center" class="images-project">
											<v-col class="d-flex child-flex" cols="12" lg="6">
												<v-img src="../assets/project_agrotehc2.png" aspect-ratio="1" class="lighten-2" contain>
													<template v-slot:placeholder>
														<v-row class="fill-height ma-0" align="center" justify="center">
															<v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
														</v-row>
													</template>
												</v-img>
											</v-col>
											<v-col class="d-flex child-flex" cols="12" lg="6">
												<v-img src="../assets/project_agrotehc3.png" class="lighten-2" contain>
													<template v-slot:placeholder>
														<v-row align="center" justify="center">
															<v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
														</v-row>
													</template>
												</v-img>
											</v-col>
										</v-row>
									</v-container>
								</div>
							</v-dialog>
						</v-card-title>
					</v-card>
				</v-col>

				<!--Site Âncora-->
				<v-col cols="10" sm="5" lg="5" class="project-item">
					<v-card>
						<v-img src="../assets/ancora.png" max-height="125" contain></v-img>
						<v-card-title class="text-h6">
							<v-dialog class="dialog-here" v-model="dialog2" fullscreen hide-overlay transition="dialog-bottom-transition">
								<template v-slot:activator="{ on, attrs }">
									<div class="data-project">
										<h5 class="title-project hvr-pop" v-bind="attrs" v-on="on">E-Commerce Âncora</h5>
										<p class="text-project">Website institucional e e-commerce Âncora Soluções</p>
									</div>
								</template>
								<div class="content-post-project-father" :style="`background-color: ${$route.params.cor}; color: ${$route.params.cor_letras}`">
									<v-toolbar dark color="#e59447">
										<v-btn icon dark @click="dialog2 = false">
											<v-icon>mdi-close</v-icon>
										</v-btn>
									</v-toolbar>
									<v-container>
										<v-row justify="center">
											<v-col cols="12" lg="7">

												<div class="d-flex justify-content-around content-post-project">
													<div>
														<h4>Webiste e E-Commerce Âncora Soluções</h4>
														<div class="ml-2">
															<h6 class="d-flex">
																<i class="fas fa-laptop"></i>&nbsp;Windows/MacOS/Linux/iOS/Android
															</h6>
															<h6 class="d-flex">
																<i class="far fa-keyboard"></i>&nbsp;HTML5//CSS3/WordPress/PHP
															</h6>
															<h6 class="d-flex">
																<i class="fas fa-external-link-alt"></i>&nbsp;solucoesancora.com.br
															</h6>
														</div>
													</div>
													<div class="about-project">
														<p>O Webiste e e-commerce foi criado com um layout único, e personalizado de acordo com as cores da empresa e mantendo o aspecto sério da área de atuação. Website contando com uma loja integrada, feita com Woocommerce, cadastro fácil de novos produtos, e site totalmente personalizável através do painel administrativo do WordPress. Área de contato, e botão flutuante do WhatsApp para entrar em contato com os resposáveis da empresa.</p>
													</div>
												</div>
											</v-col>
										</v-row>
										<v-row justify="center" class="images-project">
											<v-col class="d-flex child-flex" cols="12" lg="6">
												<v-img src="../assets/project_ancora.png" aspect-ratio="1" class="lighten-2" contain>
													<template v-slot:placeholder>
														<v-row class="fill-height ma-0" align="center" justify="center">
															<v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
														</v-row>
													</template>
												</v-img>
											</v-col>
											<v-col class="d-flex child-flex" cols="12" lg="6">
												<v-img src="../assets/project_ancora2.png" class="lighten-2" contain>
													<template v-slot:placeholder>
														<v-row align="center" justify="center">
															<v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
														</v-row>
													</template>
												</v-img>
											</v-col>
										</v-row>
									</v-container>
								</div>
							</v-dialog>
						</v-card-title>
					</v-card>
				</v-col>

				<!--Site Câmara Charrua-->
				<v-col cols="10" sm="5" lg="5" class="project-item">
					<v-card>
						<v-img src="../assets/project_camara.png" max-height="125" contain></v-img>
						<v-card-title class="text-h6">
							<v-dialog class="dialog-here" v-model="dialog4" fullscreen hide-overlay transition="dialog-bottom-transition">
								<template v-slot:activator="{ on, attrs }">
									<div class="data-project">
										<h5 class="title-project hvr-pop" v-bind="attrs" v-on="on">Site Câmara Charrua</h5>
										<p class="text-project">Site institucional e blog Câmara municipal de Charrua, painel administrativo WordPress
										</p>
									</div>
								</template>
								<div class="content-post-project-father" :style="`background-color: ${$route.params.cor}; color: ${$route.params.cor_letras}`">
									<v-toolbar dark color="#e59447">
										<v-btn icon dark @click="dialog4 = false">
											<v-icon>mdi-close</v-icon>
										</v-btn>
									</v-toolbar>
									<v-container>
										<v-row justify="center">
											<v-col cols="12" lg="7">

												<div class="d-flex justify-content-around content-post-project">
													<div>
														<h4>Site Câmara Municipal de Charrua RS</h4>
														<div class="ml-2">
															<h6 class="d-flex">
																<i class="fas fa-laptop"></i>&nbsp;Windows/MacOS/Linux/iOS/Android
															</h6>
															<h6 class="d-flex">
																<i class="far fa-keyboard"></i>&nbsp;HTML5//CSS3/WordPress/PHP/Vue.JS
															</h6>
															<h6 class="d-flex">
																<i class="fas fa-external-link-alt"></i>&nbsp;camaracharrua.rs.gov.br
															</h6>
														</div>
													</div>
													<div class="about-project">
														<p>O site foi desenvolvido com o intuito de uma maneira fácil e rápida de fazer postagens e acontecimentos da cidade. Postagens listadas por categorias, página de contato via formulário, e painel administrativo WordPress.</p>
													</div>
												</div>
											</v-col>
										</v-row>
										<v-row justify="center" class="images-project">
											<v-col class="d-flex child-flex" cols="12" lg="6">
												<v-img src="../assets/project_camara2.png" aspect-ratio="1" class="lighten-2" contain>
													<template v-slot:placeholder>
														<v-row class="fill-height ma-0" align="center" justify="center">
															<v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
														</v-row>
													</template>
												</v-img>
											</v-col>
											<v-col class="d-flex child-flex" cols="12" lg="6">
												<v-img src="../assets/project_camara3.png" class="lighten-2" contain>
													<template v-slot:placeholder>
														<v-row align="center" justify="center">
															<v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
														</v-row>
													</template>
												</v-img>
											</v-col>
										</v-row>
									</v-container>
								</div>
							</v-dialog>
						</v-card-title>
					</v-card>
				</v-col>

				<!--Site SuporTI-->
				<v-col cols="10" sm="5" lg="5" class="project-item">
					<v-card>
						<v-img src="../assets/project_suporti.png" max-height="125" contain></v-img>
						<v-card-title class="text-h6">
							<v-dialog class="dialog-here" v-model="dialog3" fullscreen hide-overlay transition="dialog-bottom-transition">
								<template v-slot:activator="{ on, attrs }">
									<div class="data-project">
										<h5 class="title-project hvr-pop" v-bind="attrs" v-on="on">Website SuporTI</h5>
										<p class="text-project">Site institucional SuporTI e administração de conteúdo WordPress
										</p>
									</div>
								</template>
								<div class="content-post-project-father" :style="`background-color: ${$route.params.cor}; color: ${$route.params.cor_letras}`">
									<v-toolbar dark color="#e59447">
										<v-btn icon dark @click="dialog3 = false">
											<v-icon>mdi-close</v-icon>
										</v-btn>
									</v-toolbar>
									<v-container>
										<v-row justify="center">
											<v-col cols="12" lg="7">

												<div class="d-flex justify-content-around content-post-project">
													<div>
														<h4>Website Institucional SuporTI</h4>
														<div class="ml-2">
															<h6 class="d-flex">
																<i class="fas fa-laptop"></i>&nbsp;Windows/MacOS/Linux/iOS/Android
															</h6>
															<h6 class="d-flex">
																<i class="far fa-keyboard"></i>&nbsp;HTML5//CSS3/WordPress/PHP/
															</h6>
															<h6 class="d-flex">
																<i class="fas fa-external-link-alt"></i>&nbsp;suportisolucoes.com.br
															</h6>
														</div>
													</div>
													<div class="about-project">
														<p>Site para mostrar serviços feitos pela SuporTI e ser uma forma de contato com a empresa. Todo o conteúdo do site é personalizável através do painel administrativo WordPress.</p>
													</div>
												</div>
											</v-col>
										</v-row>
										<v-row justify="center" class="images-project">
											<v-col class="d-flex child-flex" cols="12" lg="6">
												<v-img src="../assets/project_suporti2.png" aspect-ratio="1" class="lighten-2" contain>
													<template v-slot:placeholder>
														<v-row class="fill-height ma-0" align="center" justify="center">
															<v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
														</v-row>
													</template>
												</v-img>
											</v-col>
											<v-col class="d-flex child-flex" cols="12" lg="6">
												<v-img src="../assets/project_suporti3.png" class="lighten-2" contain>
													<template v-slot:placeholder>
														<v-row align="center" justify="center">
															<v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
														</v-row>
													</template>
												</v-img>
											</v-col>
										</v-row>
									</v-container>
								</div>
							</v-dialog>
						</v-card-title>
					</v-card>
				</v-col>

			</v-row>
			<v-row justify="center" style="margin-top: 20px">
				<h6>Certificados</h6>
			</v-row>
			<v-row justify="center">
				<!--Tem que fazer loop com isso aqui (vergonha)-->
				<v-col  cols="10" sm="5" lg="5">
					<div>
						<v-img class="img-certificate" @click="overlay1 = !overlay1" width="265" src="../assets/certificados/certificado1.png"></v-img>
						<v-overlay :value="overlay1">
							<v-img class="img-certificate-great-size" @click="overlay1 = !overlay1" src="../assets/certificados/certificado1.png"></v-img>
						</v-overlay>
					</div>
				</v-col>
				<v-col  cols="10" sm="5" lg="5">
					<div>
						<v-img class="img-certificate" @click="overlay2 = !overlay2" width="265" src="../assets/certificados/certificado2.png"></v-img>
						<v-overlay :value="overlay2">
							<v-img class="img-certificate-great-size" @click="overlay2 = !overlay2" src="../assets/certificados/certificado2.png"></v-img>
						</v-overlay>
					</div>
				</v-col>
				<v-col  cols="10" sm="5" lg="5">
					<div>
						<v-img class="img-certificate" @click="overlay3 = !overlay3" width="265" src="../assets/certificados/certificado3.png"></v-img>
						<v-overlay :value="overlay3">
							<v-img class="img-certificate-great-size" @click="overlay3 = !overlay3" src="../assets/certificados/certificado3.png"></v-img>
						</v-overlay>
					</div>
				</v-col>
				<v-col  cols="10" sm="5" lg="5">
					<div>
						<v-img class="img-certificate" @click="overlay4 = !overlay4" width="265" src="../assets/certificados/certificado4.png"></v-img>
						<v-overlay :value="overlay4">
							<v-img class="img-certificate-great-size" @click="overlay4 = !overlay4" src="../assets/certificados/certificado4.png"></v-img>
						</v-overlay>
					</div>
				</v-col>
			</v-row>
		</v-container>
	</div>
</template>

<script>
export default {
	data() {
		return {
			//temp
			dialog: false,
			dialog1: false,
			dialog2: false,
			dialog3: false,
			dialog4: false,

			//temp
			overlay1: false,
			overlay2: false,
			overlay3: false,
			overlay4: false,
			notifications: false,
			sound: true,
			widgets: false,
			items: [
				'https://swiperjs.com/demos/images/nature-1.jpg',
				'https://swiperjs.com/demos/images/nature-1.jpg',
			],
			index: null,
			overlay: false,
			certificates: [
				{
					img: "../assets/certificados/certificado1.png",
					overlay: {
						overlay1: false
					}
				},
				{
					img: "../assets/certificados/certificado2.png",
					overlay: {
						overlay2: false
					}
				},
				{
					img: "../assets/certificados/certificado3.png",
					overlay: {
						overlay3: false
					}
				},
				{
					img: "../assets/certificados/certificado4.png",
					overlay: {
						overlay4: false
					}
				},
			]
		}

	},
	created() {
		const viewportMeta = document.createElement('meta');
		viewportMeta.name = 'viewport';
		viewportMeta.content = 'width=device-width, initial-scale=1';
		document.head.appendChild(viewportMeta);
	},
	name: "Portfolio"

}

</script>

<style scoped>
.data-project {
	line-height: 1;
	text-align: center;
}

.text-project {
	font-size: 16px !important;
	font-weight: normal;

}

.content-post-project-father {
	background-color: white;
	min-height: 100vh;
}

.content-post-project {
	margin-top: 30px;
}

i {
	color: var(--laranja);
}

.fa-expand-alt {
	color: black;
}

.about-project {
	margin-left: 200px;
}

.images-project {
	margin-top: -100px;
}

.v-card {
	min-height: 230px;
	min-width: 210px;
}

.title-project {
	font-size: 18px;
}

.about-project {
	text-align: end;
}


/*Estilo somente MD*/
@media (min-width: 768px) and (max-width: 991px) {

	.about-project {
		margin-left: 100px;
	}

}

/*Estilo somente LG*/
@media (min-width: 992px) and (max-width: 1199px) {
	.about-project {
		margin-left: 150px;
	}
}

/*Estilo somente XS*/
@media (min-width: 0) and (max-width: 575px) {

	.project-item {
		display: flex;
		justify-content: center;
	}

	.about-project {
		margin: 0;
	}

	.content-post-project {
		flex-direction: column;
	}

	.images-project {
		margin-top: 0;
	}

	.about-project {
		margin-top: 10px;
		text-align: center;
	}

	.data-oculted {
		margin-top: 10px;
	}
	.img-certificate-great-size{
		width: 350px;
	}
}

.img-certificate,
.img-certificate-great-size {
	cursor: pointer;
}

.img-certificate {
	border-radius: 5px;
}
.text-h6{
	font-family: 'Poppins', sans-serif!important;
}
</style>