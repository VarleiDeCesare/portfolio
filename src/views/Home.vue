<template>
	<div>
		<div class="row">
			<div class="col">
				<div class="d-flex justify-content-around">
					<div id="name-cargo">
						<h4>Varlei De Cesare</h4>
						<p>Full-Stack Developer (Laravel/Vue.js/WordPress/PHP)</p>
					</div>
					<div>
						<!--todo aqui tem que colocar uma foto minha-->
						<!--<img src="" alt="">-->
						<!--						<i class="fas fa-user fa-3x"></i>-->
						<v-avatar class="hvr-float" height="75px" width="75px">
							<img src="../assets/emojijpeg.jpeg">
						</v-avatar>
					</div>
				</div>
			</div>
		</div>
		<div class="row">
			<div class="col col-aling-center-mobile">
				<h5 id="title-works">Sobre mim</h5>
				<p id="about-me">&nbsp;&nbsp;&nbsp;&nbsp;Sou desenvolvedor Full-Stack, trabalhando com as tecnologias Laravel PHP e Vue.js. Atualmente trabalho como terceiro para a empresa Ejetar na criação de sites com painéis administrativos. Sites criados com HTML/5 CSS/3 e Bootstrap para lidar com a responsividade, painel para administrar as informações do site feito com WordPress.</p>
			</div>
		</div>
		<div class="row">
			<div class="col col-aling-center-mobile">
				<h5 id="title-bio">Bio</h5>
				<ul id="me-bio">
					<li><i class="fas fa-map-marker-alt fa-lg link"></i> Água Santa, Rio Grande do Sul - Brasil</li>
					<li><i class="fas fa-university fa-lg link" style="margin-left: -4px"></i> 4° Semestre de Ciências da Computação - Imed</li>
					<li><i class="fas fa-code-branch fa-lg link"></i> Experiência como desenvolvedor FullStack - Ejetar</li>
				</ul>
			</div>
		</div>
		<div class="row">
			<div class="col col-aling-center-mobile">
				<h5 id="title-social-media">Redes Sociais</h5>
				<ul id="me-social-media">
					<li>
						<a href="https://github.com/VarleiDeCesare"><i class="fab fa-github fa-lg link hvr-pop"></i></a>
						@VarleiDeCesare
					</li>

					<li>
						<a href="https://www.instagram.com/varlei_cesare/"><i class="fab fa-instagram fa-lg link hvr-pop"></i></a>
						@varlei_cesare
					</li>
<!--					<li>-->
<!--						<a href="wa.me/5554991091980"><i class="fab fa-whatsapp fa-lg link hvr-pop"></i></a>-->
<!--						Varlei De Cesare-->
<!--					</li>-->
				</ul>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Home',

	components: {},
	data(){
		return {
			cor_letras: "black"
		}
	}
}
</script>
<style>
:root{
	--laranja: #e59447
}
.link{
	color: var(--laranja)
}

#title-welcome {
	margin: 50px 0;
	padding: 13px 100px;
	border-radius: 10px;
	font-weight: unset;
}

#title-works,
#title-bio,
#title-social-media{
	margin-left: 50px;
}

#about-me,
#me-bio,
#me-social-media{
	margin: 20px 0 0 55px;
	font-size: 17px;
}
ul{
	list-style: none!important;
}
li{
	font-size: 17px;
	margin-bottom: 3px;
}

.link-portfolio {
	margin-top: 20px;
}

/*Estilo somente XS*/
@media (min-width: 0) and (max-width: 575px) {
	.col-aling-center-mobile{
		display: flex;
		justify-content: center;
		flex-direction: column;
		align-items: center;
		text-align: center;
	}

	#about-me, #me-bio, #me-social-media {
		margin: 20px 0  0 0;
	}

	#title-works, #title-bio, #title-social-media {
		margin-left: 0;
	}

	#name-cargo h4{
		font-size: 20px;
	}

	#name-cargo p{
		font-size: 14px;
	}
	ul, li{
		padding: 0!important;
	}
}

</style>
