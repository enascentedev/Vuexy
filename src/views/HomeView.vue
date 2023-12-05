<script setup>
import Cabecalho from "../components/cabecalho.vue";
import Count from "../components/count.vue";
import Table from "../components/table.vue";
import Navegation from "../components/navegation.vue";
</script>

<template>
  <div class="flex h-screen">
    <aside class="w-1/5 h-full ">
      <navegation />
    </aside>
    <main class="w-4/5 h-screen flex flex-col">
      <section class="h-20 ">
        <cabecalho />
      </section>
      <section class="h-40 ">
        <count />
      </section>
      <section class="flex-1">
        <Table/>
      </section>
    </main>
  </div>
</template>
