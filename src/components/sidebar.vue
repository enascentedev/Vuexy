<template>
	<div id="main">
		<!-- mudar para h1 -->
		<h1>
			<img src="../assets/logo.png"  />
			<font-awesome-icon :icon="['fas', 'circle-dot']" class="i" />
		</h1>
		<nav class="dropdown">
			<button>
				<span>
					<font-awesome-icon :icon="['fas', 'table-cells-large']" />
					Layout
				</span>
				<font-awesome-icon :icon="['fas', 'caret-right']"/>
			</button>
			<ul class="menu" >
				<li><a>Opção 1</a></li>
				<li><a>Opção 2</a></li>
			</ul>
		</nav>
		<div class="dropdown">
			<button>
				<span >
					<font-awesome-icon :icon="['fas', 'chart-line']" />
					Dashboard
				</span>
				<font-awesome-icon :icon="['fas', 'caret-right']"/>
			</button>
			<ul class="menu">
				<li><a>Opção 3</a></li>
				<li><a>Opção 4</a></li>
			</ul>
		</div>
	</div>
</template>

<script>
export default {
	name: "Sidebar",
};
</script>
<style lang="postcss" scoped>
#main{
	@apply h-full flex flex-col gap-3 items-center p-5;
	.i {
	@apply flex justify-end
	}
	.dropdown {
  @apply w-full h-20;

}
	.dropdown button{
	@apply flex justify-between items-center w-full text-gray-700 p-2 ;
}
.dropdown button span{
	@apply flex flex-1 gap-2 items-center text-xl;
}

}
#main > h1:first-of-type {
	@apply w-full flex justify-between items-center p-1;
}

#main > nav {
	@apply flex justify-end items-center gap-5;
}
#main a {
	@apply text-sm;
}
ul {
	@apply shadow menu dropdown-content bg-base-100 rounded-box w-full z-50;
}
</style>
