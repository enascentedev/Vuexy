<script setup>
import Header from "@/components/header.vue";
import Dashboard from "@/components/dashboard.vue";
import Navegation from "@/components/navegation.vue";
import Footer from "@/components/footer.vue";
</script>

<template>
  <div class="h-full flex flex-col "> 
    <div class="flex flex-1"> 
      <aside class="w-1/5">
        <navegation />
      </aside>
      <main class="w-4/5 flex flex-col bg-gray-200">
        <section class="h-20 mx-10 my-5">
          <Header/>
        </section>
        <section class="px-10">
          <Dashboard />
        </section>
			
      </main>
    </div>
  </div>
	<footer class="w-ful bg-gray-400">
		<Footer/>
	</footer>
</template>

