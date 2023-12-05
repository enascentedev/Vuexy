<script setup>
import Cabecalho from "../components/cabecalho.vue";
import Count from "../components/count.vue";
import Table from "../components/table.vue";
import Navegation from "../components/navegation.vue";
import Footer from "../components/footer.vue";
</script>

<template>
  <div class="flex flex-col min-h-screen"> <!-- Altere para flex-col e min-h-screen -->
    <div class="flex flex-1"> <!-- Adicione um div envolvendo aside e main -->
      <aside class="w-1/5">
        <navegation />
      </aside>
      <main class="w-4/5 flex flex-col">
        <section class="h-20">
          <cabecalho />
        </section>
        <section class="h-40">
          <count />
        </section>
        <section class="flex-1">
          <Table/>
        </section>
				<Footer/>
      </main>
    </div>
    <footer class="w-full h-40">
     
    </footer>
  </div>
</template>

