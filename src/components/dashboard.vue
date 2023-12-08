<template>
	<div class="w-full flex flex-col gap-5" >
		<div class="w-full grid grid-cols-4 gap-5 ">
			<!-- primeira linha  -->
			<section class="col-span-2 bg-blue-500 h-64 py-10 px-5 rounded-lg">
				<div class="flex text-amber-50">
					<div class="w-2/3">
						<div class="flex flex-col font-semibold ">
							<h3>Website Analytics</h3>
							<p>Total 28.5%</p>
							<h3 class="mt-5">Traffic</h3>
						</div>
						<div class="flex items-center gap-1 mt-5 ">
							<span class="px-2 py-1 rounded-lg bg-blue-900">28%</span>
							<p>Sessions</p>
							<span class="px-2 py-1 rounded-lg bg-blue-900">3.1k</span>
							<p>Page Views</p>
						</div>
						<div class="flex items-center gap-3 mt-5">
							<span>28%</span>
							<p>Sessions</p>
							<span>3.1k</span>
							<p>Page Views</p>
						</div>

					</div>
					<div class="w-1/3 h-full mt-10 mr-10">
						<img src="https://demos.pixinvent.com/vuexy-html-admin-template/assets/img/illustrations/card-website-analytics-1.png" alt="Descrição da Imagem"/>
				</div>

				</div>

			</section>
			<span class="col-span-1 bg-red-600 h-64  rounded-lg"></span>
			<span class="col-span-1 bg-amber-400 h-64 rounded-lg"></span>
		</div>

		<!-- segunda linha -->
		<section class="w-full grid grid-cols-3 gap-5">
			<span class="h-96 col-span-1 py-10 px-5 rounded-lg bg-white">
				<div class="flex items-center gap-20 p-2">
						<div>
							<h3>Sales by Countries</h3>
							<p class="text-xs">Monthly Sales Overview</p>
						</div>
						<font-awesome-icon :icon="['fas', 'ellipsis-vertical']"  class="flex flex-1"/>
				</div>
				<div class="flex items-center  p-2">
					<font-awesome-icon :icon="['fas', 'flag-usa']" class="p-3 rounded-full  bg-yellow-400" />
					<div class="flex flex-1 p-2">
						<div class="flex flex-col">
							<span class="font-semibold text-lg">$8,567k</span>
							<span class="text-sm text-gray-600">United States</span>
						</div>
					</div>

					
					<div class="flex gap-2 items-center ">
						<font-awesome-icon :icon="['fas', 'caret-up']" />
						<span class="font-semibold">25.8%</span>
					</div>

				</div>
				<div class="flex items-center gap-20 p-2">
						<div>
							<h3>Sales by Countries</h3>
							<p class="text-xs">Monthly Sales Overview</p>
						</div>
						<font-awesome-icon :icon="['fas', 'ellipsis-vertical']"  class="flex flex-1"/>
				</div>
				<div class="flex items-center  p-2">
					<font-awesome-icon :icon="['fas', 'flag-usa']" class="p-3 rounded-full  bg-yellow-400" />
					<div class="flex flex-1 p-2">
						<div class="flex flex-col">
							<span class="font-semibold text-lg">$8,567k</span>
							<span class="text-sm text-gray-600">United States</span>
						</div>
					</div>

					
					<div class="flex gap-2 items-center ">
						<font-awesome-icon :icon="['fas', 'caret-up']" />
						<span class="font-semibold">25.8%</span>
					</div>

				</div>

			</span>
			<span class="h-64 col-span-1 py-10 px-5 rounded-lg bg-white">
				<div class="flex items-center gap-20 p-2">
						<div>
							<h3>Source Visits</h3>
							<p class="text-xs">38.4k Visitors</p>
						</div>
						<font-awesome-icon :icon="['fas', 'ellipsis-vertical']"  class="flex flex-1"/>
				</div>
				<div class="flex items-center  p-2">
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

			<span class="h-64 col-span-1 rounded-lg bg-white">
				<div class="h-full flex items-center justify-center">
					<p class="text-center">
						Developer
					</p>
				</div>
			</span>
		</section>

<!-- terceira linha -->
		<section class="w-full grid grid-cols-3 gap-5 ">
			<span class="h-96 col-span-1 py-10 px-5 rounded-lg bg-white">
				<div class="flex items-center gap-20 p-2">
						<div>
							<h3>Source Visits</h3>
							<p class="text-xs">38.4k Visitors</p>
						</div>
						<font-awesome-icon :icon="['fas', 'ellipsis-vertical']"  class="flex flex-1"/>
				</div>
				<div class="flex items-center  p-2">
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
							<h1 class="text-xl font-semibold">Projects</h1>
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
									<!-- Linhas da Tabela -->
									<tr class="border-b bg-gray-50">
										<td class="w-4 p-4">
											<div class="flex items-center">
												<input type="checkbox" class="form-checkbox">
											</div>
										</td>
										<td class="px-6 py-4">
											<!-- Seu conteúdo aqui -->
										</td>
										<td class="px-6 py-4">
											<!-- Seu conteúdo aqui -->
										</td>
										<td class="px-6 py-4">
											<!-- Seu conteúdo aqui -->
										</td>
										<td class="px-6 py-4">
											<!-- Seu conteúdo aqui -->
										</td>
										<td class="px-6 py-4">
											<!-- Seu conteúdo aqui -->
										</td>
									</tr>
									<!-- Repita para outras linhas -->
								</tbody>
							</table>
						</div>
					</div>

				</section>
		</section>




	</div>
</template>

<script>
export default {
	name: "Count",
};
</script>
