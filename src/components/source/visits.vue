<template>
<div id="visits">
	<section >
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
</div>
</template>

<script>
export default {
	name: "Visits",
};
</script>

<style lang="postcss" scoped>
#visits {
	 section{
		@apply h-96 col-span-1 rounded-lg ;
		.title{
			@apply flex flex-1;
			div{
				@apply flex flex-col;
				p{
					@apply text-xs;
				}
			}
		}
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
}
</style>