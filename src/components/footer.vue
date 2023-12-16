<template>
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
	@apply flex justify-between p-5 bg-slate-400;
}
#footer > div:first-of-type {
	@apply flex justify-start items-center gap-3;
}
#footer > nav {
	@apply flex justify-end items-center gap-5;
}
#footer a {
	@apply text-sm;
}
</style>
