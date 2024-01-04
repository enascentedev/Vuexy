<template>
	<div id="sidebar">
		<h1>
			<img src="../assets/logo.png"  />
			<font-awesome-icon :icon="['fas', 'circle-dot']" class="i" />
		</h1>
		<nav class="dropdown">
			<ul>
				<li>
					<font-awesome-icon :icon="['fas', 'table-cells-large']" />
					Layout
				</li>
				<font-awesome-icon :icon="['fas', 'caret-right']"/>
			</ul>
			<ul class="menu teste" >
				<li><a>Opção 1</a></li>
				<li><a>Opção 2</a></li>
			</ul>
		</nav>
		
	</div>
</template>

<script>
export default {
	name: "Sidebar",
};
</script>
<style lang="postcss" scoped>
#sidebar{
	@apply h-full flex flex-col gap-3 items-center p-5;
	.i {
	@apply flex justify-end
	}
	.dropdown {
  @apply w-full ;

}
	.dropdown ul{
	@apply relative flex justify-between items-center w-full text-gray-700 p-2 ;
}
.dropdown li{
	@apply relative flex flex-1 gap-2 items-center text-xl;
}

}
#sidebar > h1:first-of-type {
	@apply w-full flex justify-between items-center p-1;
}

#sidebar > nav {
	@apply flex justify-end items-center gap-5;
}
#sidebar a {
	@apply text-sm;
}
.teste{
	@apply shadow menu dropdown-content bg-base-100 rounded-box w-full z-50;
}
</style>
