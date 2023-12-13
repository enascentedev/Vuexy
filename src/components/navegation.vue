<template>
	<!-- mudar nomenclatura para sidebar -->
	<div id="main">
		<!-- mudar para h1 -->
		<div>
			<img src="../assets/logo.png"  />
			<font-awesome-icon :icon="['fas', 'circle-dot']" class="i" />
		</div>
		<nav class="dropdown">
			<button>
				<span>
					<font-awesome-icon :icon="['fas', 'table-cells-large']" />
					Layout
				</span>
				<font-awesome-icon :icon="['fas', 'caret-right']"/>
			</button>
			<ul class="menu" >
				<li><a>Item 1</a></li>
				<li><a>Item 2</a></li>
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
				<li><a>Item 1</a></li>
				<li><a>Item 2</a></li>
			</ul>
		</div>
	</div>
</template>

<script>
export default {
	name: "Navigation",
};
</script>
<style lang="postcss" scoped>
#main{
	@apply h-full flex flex-col gap-3 items-center p-5;
	.i {
	@apply flex justify-end
	}
	.dropdown {
  @apply w-full;

}
	.dropdown button{
	@apply flex justify-between items-center w-full text-gray-700 p-2 ;
}
.dropdown button span{
	@apply flex flex-1 gap-2 items-center text-xl;
}

}
#main > div:first-of-type {
	@apply w-full flex justify-between items-center p-1;
}

#main > nav {
	@apply flex justify-end items-center gap-5;
}
#main a {
	@apply text-sm;
}
ul {
	@apply pt-20 shadow menu dropdown-content bg-base-100 rounded-box w-full;
}
</style>
