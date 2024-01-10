<template>

	<div id="dashboard">
		<!-- first line -->
		<section class="row-one">
			<section>
				<chartBar/>
			</section>
			<div class="col-two">
				<chartPie/>
			</div>
			<div class="col-three">
				<chartRadial/>
			</div>
		</section>

		<!-- second line -->
		<section class="row-two">
			<span class="col-one">
				<Visits/>
			</span>

			<div class="col-one">
				<chartBarra/>
			</div>

			<div class="col-one">
				<chartMap/>
			</div>
		</section>

<!-- third line -->
		<section class="row-three">
			<span class="col-one">
				<chartBrand/>
			</span>
				<div class="col-table">
				<Table/>
				</div>
		</section>
	</div>
</template>

<script>
import chartPie from "@/components/graficos/chartPie.vue";
import chartRadial from "@/components/graficos/chartRadial.vue";
import chartBarra from "@/components/graficos/chartBarra.vue";
import chartBar from "@/components/graficos/chartBar.vue";
import chartMap from "@/components/graficos/chartMap.vue";
import chartBrand from "@/components/graficos/chartBrand.vue";
import Visits from "@/components/source/visits.vue";
import Table from "@/components/table.vue";

export default {
	name: "Dashboard",
	components: {
		chartPie,
		chartRadial,
		chartBarra,
		chartBar,
		chartMap,
		chartBrand,
		Table,
		Visits,
	},
};
</script>
<style lang="postcss" scoped>
#dashboard {
  @apply w-full flex flex-col gap-5;
 .row-one{
	@apply w-full grid grid-cols-4 gap-5;
		section{
		@apply col-span-2 h-64 py-10 px-5 rounded-lg bg-white;
		}
		.col-two,.col-three{
		@apply h-64  p-5 rounded-lg bg-white;  
	}
}
.row-two{
  @apply w-full grid grid-cols-3 gap-5;
}
}
.row-three{
  @apply w-full grid grid-cols-3 gap-5 mb-5;
}
.col-one {
		@apply h-64 col-span-1 rounded-lg bg-white;
	}
	.col-table {
		@apply h-64 col-span-2 rounded-lg bg-slate-500;
	}
</style>
