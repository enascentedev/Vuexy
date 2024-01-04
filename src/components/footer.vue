<template>
	<!-- adicionr ul e li na lista de <a> -->]
		<!-- analisar tag adress e seu uso no contexto -->
	<footer id="footer">
		<div>
			<span>2023, made in brazil</span>
			<a>Sintax</a>
		</div>
		<nav>
			<a>Licensa</a>
			<a>Documentação</a>
			<a>Suporte</a>
			<a>contato</a>
		</nav>
	</footer>
</template>

<script>
export default {
	name: "Footer",
};
</script>

<style lang="postcss" scoped>
#footer {
	@apply h-20 flex justify-between p-5 bg-slate-400;

	div:first-of-type {
		@apply flex justify-start items-center gap-3;
	}
	nav {
		@apply flex justify-end items-center gap-5;
	}
	a {
		@apply text-sm;
	}
}
</style>
