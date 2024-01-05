<template>
	<div id="sidebar">
		<h1>
			<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRmg6VbQr7k4bE8m1sGjODK19nEZn-UKVChBg&usqp=CAU" alt="logoe" />
			<font-awesome-icon :icon="['fas', 'circle-dot']" class="i" />
		</h1>
		<nav class="list">
			<ul>
				<li>
					<a href="#">
						<font-awesome-icon :icon="['fas', 'table-columns']" />
						Layout
					</a>
					<font-awesome-icon :icon="['fas', 'caret-right']"/>
				</li>
				<li>
					<a href="#">
						<font-awesome-icon :icon="['far', 'envelope']" />
						Email
					</a>
					<font-awesome-icon :icon="['fas', 'caret-right']"/>
				</li>
				<li>
					<a href="#">
						<font-awesome-icon :icon="['fas', 'cart-shopping']" />
						E-comerce
					</a>
					<font-awesome-icon :icon="['fas', 'caret-right']"/>
				</li>
				<li>
					<a href="#">
						<font-awesome-icon :icon="['fas', 'chart-pie']" />
						Gráficos
					</a>
					<font-awesome-icon :icon="['fas', 'caret-right']"/>
				</li>
				<li>
					<a href="#">
						<font-awesome-icon :icon="['fas', 'table-cells-large']"/>
						Tabelas
					</a>
					<font-awesome-icon :icon="['fas', 'caret-right']"/>
				</li>
				
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
	img{
		@apply w-20 h-20;
	}
	.i {
	@apply flex justify-end
	}
	.list {
  @apply w-full ;
}
	.list ul{
	@apply w-full flex flex-col items-center text-gray-700 p-2 ;
}
.list li{
	@apply w-full h-10 flex justify-between gap-2 items-center text-xl;
	a {
		@apply flex gap-5 items-center ;
	}
}
}
 h1{
	@apply w-full flex justify-between items-center p-1;
}
 nav {
	@apply flex justify-end items-center gap-5;
}

</style>
