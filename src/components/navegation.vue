<template>
	<div class="h-full flex flex-col gap-10 items-center py-12">
		<address class="flex flex-col items-center gap-1 p-5 not-italic">
			<i class="fas fa-user-circle p-2 text-6xl"></i>
			<p>Emanuel</p>
			<p>Email: <a href="mailto:contato@exemplo.com">manequinha@.com</a></p>
		</address>
		<nav class="flex flex-col gap-10 text-base">
			<a href="#"><i class="fas fa-house pr-2"></i>home </a>
			<a href="#"><i class="fas fa-file pr-2"></i>File </a>
			<a href="#"><i class="fas fa-message pr-2"></i>Message </a>
			<a href="#"><i class="fas fa-bell pr-2"></i>Notification</a>
			<a href="#"><i class="fas fa-location pr-2"></i>Location</a>
			<a href="#"><i class="fas fa-chart-pie pr-2"></i>Graph</a>
			
		</nav>
	</div>
</template>

<script>
export default {
	name: "Navegation",
};
</script>
