<template>
	<div class="h-full flex flex-col gap-3 items-center p-5">
		<div class="w-full flex justify-between items-center p-1">
			<img src="../assets/logo.png"  />
			<font-awesome-icon :icon="['fas', 'circle-dot']" class="flex justify-end" />
		</div>
		<div class="dropdown flex w-full">
			<button class="flex justify-between items-center w-full text-gray-700 p-2">
				<span class="flex-flex-1">
					<font-awesome-icon :icon="['fas', 'toggle-off']"/>
					Form Elements
				</span>
				<font-awesome-icon :icon="['fas', 'caret-right']"/>
			</button>
			<ul class="pt-2 shadow menu dropdown-content bg-base-100 rounded-box w-full">
				<li><a>Item 1</a></li>
				<li><a>Item 2</a></li>
			</ul>
		</div>
		<div class="dropdown flex w-full">
			<button class="flex justify-between items-center w-full text-gray-700 p-2">
				<span class="flex-flex-1">
					<font-awesome-icon :icon="['fas', 'toggle-off']"/>
					Form Elements
				</span>
				<font-awesome-icon :icon="['fas', 'caret-right']"/>
			</button>
			<ul class="pt-20 shadow menu dropdown-content bg-base-100 rounded-box w-full">
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
