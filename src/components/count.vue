<template>
	<div class="w-full h-full flex justify-between gap-5 p-4">

		<div class="w-1/6 h-32 grid grid-cols-4 gap-4 p-5 bg-sky-200">
			<span class="col-start-1 col-end-4 text-left">Erning</span>
			<i
				class="fa-regular fa-compass text-base col-start-5 col-end-6 text-right"></i>
			<span class="col-start-1 col-end-5 text-left text-5xl">$628</span>
		</div>

		<div class="w-1/6 h-32 grid grid-cols-4 gap-4 p-5 bg-sky-200">
			<span class="col-start-1 col-end-4 text-left">Share</span>
			<i
				class="fas fa-share text-base col-start-5 col-end-6 text-right"></i>
			<span class="col-start-1 col-end-5 text-left text-5xl">2434</span>
		</div>

		<div class="w-1/6 h-32 grid grid-cols-4 gap-4 p-5 bg-sky-200">
			<span class="col-start-1 col-end-4 text-left">Likes</span>
			<i
				class="fa-regular fa-thumbs-up text-base col-start-5 col-end-6 text-right"></i>
			<span class="col-start-1 col-end-5 text-left text-5xl">1259</span>
		</div>

		<div class="w-1/6 h-32 grid grid-cols-4 gap-4 p-5 bg-sky-200">
			<span class="col-start-1 col-end-4 text-left">Rating</span>
			<i
				class="fa-regular fa-star text-base col-start-5 col-end-6 text-right"></i>
			<span class="col-start-1 col-end-5 text-left text-5xl">8,5</span>
		</div>
		
	</div>
</template>

<script>
export default {
	name: "Count",
};
</script>
