<script setup>
import Header from "@/components/header.vue";
import Dashboard from "@/components/dashboard.vue";
import Sidebar from "@/components/sidebar.vue";
import Footer from "@/components/footer.vue";
</script>

<template>
  <div class="h-full flex flex-col">
    <div class="flex flex-1"> 
      <aside class="w-1/5">
        <Sidebar />
      </aside>
      <main class="h-full flex-grow w-4/5 flex flex-col bg-gray-200">
        <section class="mx-10 my-5">
          <Header/>
        </section>
        <section class="px-10 ">
          <Dashboard />
        </section>
      </main>
    </div>
    <footer class="w-full h-20 bg-slate-400">
      <Footer/>
    </footer>
  </div>
</template>


