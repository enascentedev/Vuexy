<template>
<footer class="flex justify-between p-5">
	<div class="flex justify-start items-center gap-3 ">
		<span>2023, made in brazil</span>
		<a>Sintax</a>
	</div>
	<nav class="flex justify-end items-center gap-5 " >
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
a{
	@apply text-sm
}
</style>