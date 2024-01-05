<template>
	<footer>

		<div id="logo">
			<router-link to="/">
				<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRmg6VbQr7k4bE8m1sGjODK19nEZn-UKVChBg&usqp=CAU" alt="logoe" />
			</router-link>
			<a href="https://empresa.com.br">by empresa</a>
		</div>

		<div id="info">
			<router-link to="/suporte">
				Suporte
			</router-link>
			<router-link to="/sobre">
				Sobre Equipe
			</router-link>
			<router-link to="/politica-de-privacidade">
				Política de Privacidade
			</router-link>
			<router-link to="/termos-de-uso">
				Termos de Uso
			</router-link>
		</div>

		<address id="address">
			<h5>
				<font-awesome-icon :icon="['far', 'location-dot']" class="i" />
				Endereço:
			</h5>
			<p>Av. carambola, 2030 - Conjunto 501</p>
			<p>Bairro Sarandi</p>
			<p>Porto Alegre, RS - Cep: 91120-600</p>
		</address>

		<address id="contact">
			<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRmg6VbQr7k4bE8m1sGjODK19nEZn-UKVChBg&usqp=CAU" alt="logo" />
			<h5>Contato:</h5>
			<p>
				<font-awesome-icon :icon="['far', 'phone']" class="i" />
				(51) 3365.5243
			</p>
			<p>
				<font-awesome-icon :icon="['far', 'envelope']" class="i" />
				<a href="mailto:contato@empresa.com.br">
					contato@empresa.com.br
				</a>
			</p>
		</address>

	</footer>
</template>

<script>
// assets


// data
export default {

	name: 'LayoutFooter',

	data() {
		return {



		}
	},

};
</script>

<style scoped postcss>
footer {
	@apply  grid grid-cols-1 gap-6 text-sm bg-white text-base-content;
	@apply md:grid-cols-2 xl:grid-cols-4;
	.i { @apply text-base-content; }
	a { @apply hover:underline; }

	#logo {
		@apply flex flex-col p-6;
		img { @apply w-32; }
		a { @apply w-32 mb-2 text-right text-xs underline; }
	}

	#info {
		@apply flex flex-col gap-2 px-6 pb-6;
		@apply xl:pt-6 md:pt-6;
	}

	#address {
		@apply px-6 pb-6 not-italic;
		@apply xl:pt-6;
		h2 { @apply flex gap-1 items-center leading-5; }
	}

	#contact {
		@apply px-6 pb-6 not-italic;
		@apply xl:pt-6;
		img { @apply w-20 mb-2; }
		p { @apply flex gap-1 items-center; }
	}
img{
	@apply h-20 w-20
}
}
</style>
