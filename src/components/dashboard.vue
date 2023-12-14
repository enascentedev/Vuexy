<template>
	
	<div id="dashboard">
		<!-- first line -->
		<section class="row-one">
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
						<img src="https://demos.pixinvent.com/vuexy-html-admin-template/assets/img/illustrations/card-website-analytics-1.png" alt="Descrição da Imagem"/>
				</div>

			</section>
			<div class="col-two ">
				<chartPie/>
			</div>
			<div class="col-three">
				<chartRadial/>
			</div>
		</section>

		<!-- second line -->
		<section class="row-two">
			<section>
				<div>
						<div class="title">
							<div>
								<h3>Sales by Countries</h3>
								<p >Monthly Sales Overview</p>
						</div>
						</div>
						<font-awesome-icon :icon="['fas', 'ellipsis-vertical']"  />
				</div>
				<div class="country">
					<font-awesome-icon :icon="['fas', 'flag-usa']" class="i"/>
					<div class="price">
						<div>
							<span>$8,567k</span>
							<p>United States</p>
						</div>
					</div>

					
					<div class="percent">
						<font-awesome-icon :icon="['fas', 'caret-up']" />
						<p>25.8%</p>
						<span>+3.1k</span>
					</div>

				</div>
			</section>

			<div class="h-64 p-5 col-span-1  rounded-lg bg-white">
				<chartBarra/>
			</div>

			<div class="h-64 col-span-1 rounded-lg bg-white">
				<chartMap/>
			</div>

		</section>

<!-- third line -->
		<section class="row-tres">
			<span class="h-96 col-span-1 py-10 px-5 rounded-lg bg-white">
				<chartBrand/>
			</span>

				<!-- table -->
				<section class="h-64 col-span-2 rounded-lg bg-slate-500 ">
		
					<div class="title-table">
						<h2>Projetos</h2>
						<input type="text" placeholder="Pesquisar:" >
					</div>
				
					<div id="content-table">
						<table>
							<thead>
								<tr>
									<th>
										<div>
											<input type="checkbox" class="form-checkbox">
										</div>
									</th>
									<th>Name</th>
									<th>Leader</th>
									<th>Team</th>
									<th>Status</th>
									<th>Actions</th>
								</tr>
							</thead>
							<tbody>
								
								<tr>
									<td >
										<div>
											<input type="checkbox" class="form-checkbox">
										</div>
									</td>
									<td>
										
									</td>
									<td>
										
									</td>
									<td>
										
									</td>
									<td>
										
									</td>
									<td>
										
									</td>
								</tr>
					
							</tbody>
						</table>
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
import chartBrand from "@/components/graficos/chartBrand.vue";

export default {
	name: "Dashboard",
	components: {
		chartPie,
		chartRadial,
		chartBarra,
		chartMap,
		chartBrand,
	},
};
</script>
<style lang="postcss" scoped>
#dashboard {
  @apply w-full flex flex-col gap-5;
 .row-one{
  @apply w-full grid grid-cols-4 gap-5;
	.col-two,.col-three{
	@apply h-64  p-5 rounded-lg bg-white;  
}
}
.row-two{
  @apply w-full grid grid-cols-3 gap-5;
}
}
.row-two section{
	@apply h-96 col-span-1 py-10 px-5 rounded-lg bg-white;
	.country {
		@apply flex items-center;
		.i{
			@apply p-3 rounded-full  bg-yellow-400
		}
		.price{
			@apply flex flex-1 p-2;
			div{
				@apply flex flex-col;
				span{
					@apply font-semibold text-lg;
				}
				p{
					@apply text-sm text-gray-600;
				}
			}
		}
		.percent{
			@apply flex items-center gap-2 font-semibold ;
			span{
				@apply px-2 py-1 rounded-lg bg-blue-600;
			}
		}
	}
}
.row-two section div:first-child{
		@apply flex items-center;
		.title{
			@apply flex flex-1;
			div{
				@apply flex flex-col;
				p{
					@apply text-xs;
				}
			}
		}

	}
.row-one section{
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
			@apply w-20 h-40 flex flex-1 mr-10; 
		}
	}
	.title-table{
		@apply flex justify-between items-center p-5;
		h2{
			@apply text-xl font-semibold
		}
		input{
			@apply h-10 px-5 border-2 border-gray-300 bg-white  rounded-lg text-sm 
		}
	}
	#content-table{
		@apply overflow-x-auto bg-white rounded-lg shadow m-5;
		table{
			thead{
				@apply text-xs text-gray-700 uppercase;
				th{
					@apply px-6 py-3;
					div{
						@apply flex items-center;
					}
				}
			}
			tbody{
				tr{
					@apply border-b bg-gray-50;
					td{
						@apply px-6 py-4;
						div{
							@apply flex items-center
						}
					}
				}
			}
		}
	}
.row-tres{
  @apply w-full grid grid-cols-3 gap-5 ;
}
</style>
