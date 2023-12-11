<template>
	<div id="dashboard">
		<!-- primeira linha -->
		<section class="row-um">
			<section>
				<div class="view">
					<div>
						<h3>Website Analytics</h3>
						<p>Total 28.5%</p>
						<h3>Traffic</h3>
					<div class="percent ">
							<span >28%</span>
							<p>Sessions</p>
							<span>3.1k</span>
							<p>Page Views</p>
						</div>
						
					</div>
						<img src="https://demos.pixinvent.com/vuexy-html-admin-template/assets/img/illustrations/card-website-analytics-1.png" alt="Descrição da Imagem" class="@apply w-1/3 h-full flex flex-1 mr-10"/>
				</div>

			</section>
			<div class="col-two ">
				<chartPie/>
			</div>
			<div class="col-three">
				<chartRadial/>
			</div>
		</section>

		<!-- segunda linha -->
		<section class="row-dois">
			<section>
				<div class="flex items-center justify-around">
						<div class="flex flex-1">
							<div class="flex flex-col">
								<h3>Sales by Countries</h3>
								<p class="text-xs">Monthly Sales Overview</p>
						</div>
						</div>
						<font-awesome-icon :icon="['fas', 'ellipsis-vertical']"  />
				</div>
				<div class="flex items-center">
					<font-awesome-icon :icon="['fas', 'flag-usa']" class="p-3 rounded-full  bg-yellow-400" />
					<div class="flex flex-1 p-2">
						<div class="flex flex-col">
							<span class="font-semibold text-lg">$8,567k</span>
							<span class="text-sm text-gray-600">United States</span>
						</div>
					</div>

					
					<div class="flex justify-end items-center gap-2">
						<font-awesome-icon :icon="['fas', 'caret-up']" />
						<span class="font-semibold">25.8%</span>
						<span class="px-2 py-1 rounded-lg bg-blue-600">+3.1k</span>
					</div>

				</div>
			</section>
			<div class="h-64 p-5 col-span-1  rounded-lg bg-white">
				<chartBarra/>

			</div>

			<span class="h-64 col-span-1 rounded-lg bg-white">
				<div class="h-full flex items-center justify-center">
					<chartMap/>
				</div>
			</span>
		</section>

<!-- terceira linha -->
		<section class="row-tres">
			<span class="h-96 col-span-1 py-10 px-5 rounded-lg bg-white">
				<div class="flex items-center gap-20 p-2">
						<div>
							<h3>Source Visits</h3>
							<p class="text-xs">38.4k Visitors</p>
						</div>
						<font-awesome-icon :icon="['fas', 'ellipsis-vertical']"  class="flex flex-1"/>
				</div>
				<div class="flex items-center">
					<font-awesome-icon :icon="['fas', 'flag-usa']" class="p-3 rounded-md bg-yellow-400" />
					<div class="flex flex-1 p-2">
						<div class="flex flex-col">
							<h3 class="font-semibold text-base">Direct Source</h3>
							<span class="text-sm text-gray-600">Direct link click</span>
						</div>
					</div>

					
					<div class="flex gap-2 items-center ">
						
						<span class="font-semibold">25.8k</span>
						<span class="px-2 py-1 rounded-lg bg-blue-600">+3.1k</span>

					</div>

				</div>

			</span>


				<section class="h-64 col-span-2 rounded-lg bg-slate-200 ">
					<div class="container mx-auto p-6">
						<!-- Título e Barra de Pesquisa -->
						<div class="flex justify-between items-center mb-6">
							<h1 class="text-xl font-semibold">Projetos</h1>
							<input type="text" placeholder="Search:" class="border-2 border-gray-300 bg-white h-10 px-5 pr-16 rounded-lg text-sm focus:outline-none">
						</div>
						
						<!-- Tabela de Projetos -->
						<div class="overflow-x-auto bg-white rounded-lg shadow">
							<table class="w-full text-sm text-left">
								<thead class="text-xs text-gray-700 uppercase bg-gray-50">
									<tr>
										<th scope="col" class="p-4">
											<div class="flex items-center">
												<input type="checkbox" class="form-checkbox">
											</div>
										</th>
										<th scope="col" class="px-6 py-3">Name</th>
										<th scope="col" class="px-6 py-3">Leader</th>
										<th scope="col" class="px-6 py-3">Team</th>
										<th scope="col" class="px-6 py-3">Status</th>
										<th scope="col" class="px-6 py-3">Actions</th>
									</tr>
								</thead>
								<tbody>
									
									<tr class="border-b bg-gray-50">
										<td class="w-4 p-4">
											<div class="flex items-center">
												<input type="checkbox" class="form-checkbox">
											</div>
										</td>
										<td class="px-6 py-4">
											
										</td>
										<td class="px-6 py-4">
											
										</td>
										<td class="px-6 py-4">
											
										</td>
										<td class="px-6 py-4">
											
										</td>
										<td class="px-6 py-4">
											
										</td>
									</tr>
							
								</tbody>
							</table>
						</div>
					</div>

				</section>
		</section>




	</div>
</template>

<script>
import chartPie from "@/components/graficos/chartPie.vue";
import chartRadial from "@/components/graficos/chartRadial.vue";
import chartBarra from "@/components/graficos/chartBarra.vue";
import chartMap from "@/components/graficos/chartMap.vue";

export default {
	name: "Dashboard",
	components: {
		chartPie,
		chartRadial,
		chartBarra,
		chartMap,
	},
};
</script>
<style lang="postcss" scoped>
#dashboard {
  @apply w-full flex flex-col gap-5;
 .row-um{
  @apply w-full grid grid-cols-4 gap-5;
	.col-two,.col-three{
	@apply h-64 col-span-1 p-5 rounded-lg bg-white;  
}
}
.row-dois{
  @apply w-full grid grid-cols-3 gap-5;
.row-dois section{
	@apply h-96 col-span-1 py-10 px-5 rounded-lg bg-white;
}
}
}
.row-um section{
		@apply col-span-2 h-64 py-10 px-5 rounded-lg bg-blue-500;
		.view{
			@apply flex text-amber-50;
			.view div {
				@apply flex flex-col font-semibold;
			}
		.percent{
			@apply flex items-center gap-1 mt-5;
			.percent span{
				@apply  px-2 py-1 rounded-lg bg-blue-900;
			}
			 h3{
					@apply mt-3;

				}
		}
		}
		img{
			@apply w-1/3 h-full flex flex-1 mr-10; 
		}
	}
#dashboard> i.fas.fa-search {
 @apply pl-5
}

.row-tres{
  @apply w-full grid grid-cols-3 gap-5 ;
}

#header > div > .fas {
  
}
</style>
