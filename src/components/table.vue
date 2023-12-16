<template>
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
              <input type="checkbox">
            </div>
          </th>
          <th >Name</th>
          <th>Leader</th>
          <th>Team</th>
          <th>Status</th>
          <th>Actions</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>
            <div>
              <input type="checkbox">
            </div>
          </td>
          <td >
						<span>Layout </span>
          </td>
          <td>
            João
          </td>
          <td>
						<font-awesome-icon :icon="['fas', 'people-group']" />
          </td>
          <td>
						<div class="radial-progress" style="--value:70; --size:4rem;" role="progressbar">70%</div>
          </td>
          <td>
						<font-awesome-icon :icon="['fas', 'bars-staggered']" />
          </td>
        </tr>
				
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
	name: "Table",
};
</script>

<style lang="postcss" scoped>
.title-table{
		@apply flex justify-between items-center p-5;
		h2{
			@apply text-xl font-semibold
		}
		input{
			@apply h-10 px-2 border-2 border-gray-300 bg-white rounded-lg text-sm ;
		}
	}
	#content-table{
		@apply  bg-white rounded-lg shadow mx-3;
		table{
			thead{
				@apply text-xs text-gray-700 uppercase;
				th{
					@apply px-9 py-3;
					div{
						@apply flex items-center;
					}
				}
			}
			tbody{
				tr{
					@apply border-b bg-gray-50;
					td{
						@apply px-9 py-3 text-center;
						div{
							@apply flex items-center
						}
					
					}
				}
			}
			icon {
    @apply mr-2;
  }
  .progress-bar {
    @apply w-full bg-gray-200 rounded-full h-2.5;
    .progress {
      @apply bg-blue-600 h-2.5 rounded-full;
    }
  }

  .team-images {
    @apply flex -space-x-1 overflow-hidden;
    img {
      @apply inline-block h-6 w-6 rounded-full ring-2 ring-white;
    }
  }

  .action-icons {
    @apply flex justify-around;
    .icon {
      @apply cursor-pointer;
   	 }
  	}
	}
}
</style>
