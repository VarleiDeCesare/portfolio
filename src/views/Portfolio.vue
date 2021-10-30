<template>
	<div>
		<v-container>
			<v-row justify="center" style="margin-top: 20px">
				<h6>Projetos</h6>
			</v-row>
			<v-row justify="center">
				<!--fixme Para cada novo post, duplique uma dessas colunas, troque os dados, troque a variavel dialog e declare a mesma no data()-->
				<!--Painel Ejetar-->
				<v-col cols="6">
					<v-card>
						<v-img src="../assets/painel.png" max-height="125" contain></v-img>
						<v-card-title class="text-h6">
							<v-dialog v-model="dialog" fullscreen hide-overlay transition="dialog-bottom-transition">
								<template v-slot:activator="{ on, attrs }">
									<div class="data-project">
										<h5 class="title-project" v-bind="attrs" v-on="on">Painel Ejetar
											<i class="fas fa-expand-alt fa-sm"></i>
										</h5>
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
											<v-col cols="7">
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
													<div class="text-end about-project">
														<p>O Painel tem o propósito de captar consumos de Disco e de Banda Larga de cada cliente, fazer o cálculo levando em consideração os gastos e lançar uma cobrança na Stripe. Stripe é a integração na qual a Stack Laravel Cashier lança a cobrança e envia e-mail com o boleto para o cliente poder fazer o pagamento</p>
													</div>
												</div>
											</v-col>
										</v-row>
										<v-row justify="center" class="images-project">
											<v-col class="d-flex child-flex" cols="6">
												<v-img src="../assets/project_painel.png" aspect-ratio="1" class="lighten-2" contain>
													<template v-slot:placeholder>
														<v-row class="fill-height ma-0" align="center" justify="center">
															<v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
														</v-row>
													</template>
												</v-img>
											</v-col>
											<v-col class="d-flex child-flex" cols="6">
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
											<small class="text-center">*Dados ocultados para proteção de dados internos*</small>
										</v-row>
									</v-container>
								</div>
							</v-dialog>
						</v-card-title>
					</v-card>
				</v-col>

				<!--CFR Agrotehc-->
				<v-col cols="6">
					<v-card>
						<v-img src="../assets/project_agrotehc.png" max-height="125" contain></v-img>
						<v-card-title class="text-h6">
							<v-dialog v-model="dialog1" fullscreen hide-overlay transition="dialog-bottom-transition">
								<template v-slot:activator="{ on, attrs }">
									<div class="data-project">
										<h5 class="title-project" v-bind="attrs" v-on="on">CFR Agrotech
											<i class="fas fa-expand-alt fa-sm"></i>
										</h5>
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
											<v-col cols="7">

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
													<div class="text-end about-project">
														<p>O aplicativo tem como propósito dar possiblidade para que produtores rurais possam cadastrar dados em suas safras de cada lavoura, para que possa ter um conhecimento maior sobre gastos, e ganhos em um único histórico, simples e funcional. O projeto ainda está em desenvolvimento e tem como ideia central o aprendizado do desenvolvedor.</p>
													</div>
												</div>
											</v-col>
										</v-row>
										<v-row justify="center" class="images-project">
											<v-col class="d-flex child-flex" cols="6">
												<v-img src="../assets/project_agrotehc2.png" aspect-ratio="1" class="lighten-2" contain>
													<template v-slot:placeholder>
														<v-row class="fill-height ma-0" align="center" justify="center">
															<v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
														</v-row>
													</template>
												</v-img>
											</v-col>
											<v-col class="d-flex child-flex" cols="6">
												<v-img src="../assets/project_agrotehc3.png" class="lighten-2" contain>
													<template v-slot:placeholder>
														<v-row align="center" justify="center">
															<v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
														</v-row>
													</template>
												</v-img>
											</v-col>
										</v-row>
<!--										<v-row>-->
<!--											<small class="text-center">*Dados ocultados para proteção de dados internos*</small>-->
<!--										</v-row>-->

									</v-container>
								</div>
							</v-dialog>
						</v-card-title>
					</v-card>
				</v-col>


			</v-row>
		</v-container>
	</div>
</template>

<script>
export default {
	data() {
		return {
			dialog: false,
			dialog1: false,
			notifications: false,
			sound: true,
			widgets: false,
		}
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

</style>